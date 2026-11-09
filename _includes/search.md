<style>
  .site-search {
    position: relative;
    margin: 0 0 1.5rem;
  }

  .site-search input {
    box-sizing: border-box;
    width: 100%;
    padding: 0.7rem 1rem;
    font-family: inherit;
    font-size: 1.1rem;
    border: 2px solid #000;
    background: #fff;
    color: #1a1a1a;
  }

  .search-results {
    position: absolute;
    top: 100%;
    left: 0;
    right: 0;
    z-index: 100;
    max-height: 70vh;
    overflow-y: auto;
    background: #fff;
    border: 2px solid #000;
    border-top: none;
  }

  .search-result {
    display: block;
    padding: 0.7rem 1rem;
    color: #1a1a1a !important;
    text-decoration: none;
    border-bottom: 1px solid #ccc;
  }

  .search-result:hover { background: #eee; }

  .search-result strong { display: block; }

  .search-result span { font-size: 0.9rem; opacity: 0.8; }

  .search-result mark { background: #ffe066; color: inherit; }

  .search-empty { padding: 0.7rem 1rem; color: #1a1a1a; }
</style>

<div class="site-search">
  <input type="search" id="site-search-input" placeholder="Search the wiki..." autocomplete="off" aria-label="Search the wiki">
  <div class="search-results" id="site-search-results" hidden></div>
</div>

<script>
(function () {
  var input = document.getElementById('site-search-input');
  var box = document.getElementById('site-search-results');
  var indexPromise = null;

  // Download the page index once, the first time it is needed.
  function loadIndex() {
    if (!indexPromise) {
      indexPromise = fetch('{{ "/search.json" | relative_url }}').then(function (r) { return r.json(); });
    }
    return indexPromise;
  }

  function escapeRegex(s) { return s.replace(/[.*+?^${}()|[\]\\]/g, '\\$&'); }

  // Build text with the search words wrapped in <mark>.
  function highlight(text, words) {
    var frag = document.createDocumentFragment();
    var re = new RegExp('(' + words.map(escapeRegex).join('|') + ')', 'gi');
    text.split(re).forEach(function (part, i) {
      if (i % 2 === 1) {
        var m = document.createElement('mark');
        m.textContent = part;
        frag.appendChild(m);
      } else {
        frag.appendChild(document.createTextNode(part));
      }
    });
    return frag;
  }

  function render(results, words) {
    box.innerHTML = '';
    if (results.length === 0) {
      var none = document.createElement('div');
      none.className = 'search-empty';
      none.textContent = 'No results found.';
      box.appendChild(none);
    }
    results.forEach(function (r) {
      var a = document.createElement('a');
      a.className = 'search-result';
      a.href = r.page.url;

      var title = document.createElement('strong');
      title.appendChild(highlight(r.page.title, words));
      a.appendChild(title);

      var lower = r.page.content.toLowerCase();
      var idx = lower.indexOf(words[0]);
      if (idx === -1) {
        for (var i = 1; i < words.length && idx === -1; i++) idx = lower.indexOf(words[i]);
      }
      if (idx !== -1) {
        var start = Math.max(0, idx - 60);
        var snippet = document.createElement('span');
        snippet.appendChild(highlight((start > 0 ? '… ' : '') + r.page.content.slice(start, start + 160) + ' …', words));
        a.appendChild(snippet);
      }
      box.appendChild(a);
    });
    box.hidden = false;
  }

  input.addEventListener('focus', loadIndex);

  input.addEventListener('input', function () {
    var query = input.value.trim().toLowerCase();
    if (query.length < 2) { box.hidden = true; return; }
    var words = query.split(/\s+/);

    loadIndex().then(function (pages) {
      var results = pages.map(function (p) {
        var t = p.title.toLowerCase();
        var c = p.content.toLowerCase();
        var score = 0;
        for (var i = 0; i < words.length; i++) {
          var inTitle = t.indexOf(words[i]) !== -1;
          var inBody = c.indexOf(words[i]) !== -1;
          if (!inTitle && !inBody) return null;   // every word must appear somewhere
          score += (inTitle ? 10 : 0) + (inBody ? 1 : 0);
        }
        return { page: p, score: score };
      }).filter(Boolean).sort(function (a, b) { return b.score - a.score; }).slice(0, 8);

      render(results, words);
    });
  });

  // Close the results when clicking anywhere else.
  document.addEventListener('click', function (e) {
    if (!e.target.closest('.site-search')) box.hidden = true;
  });
})();
</script>
