---
title: Factions
---

<style>
  .faction-grid {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
    gap: 1rem;
    margin: 2rem 0;
    width: 70vw;
    position: relative;
    left: 50%;
    transform: translateX(-50%);
  }

  .faction {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    aspect-ratio: 1 / 1;
    padding: 0.9rem 0.6rem;
    background: var(--color);
    color: #fff;
    text-decoration: none;
    text-align: center;
    border-radius: 12px;
    border: 2px solid rgba(0, 0, 0, 0.25);
    transition: transform 0.15s, box-shadow 0.15s;
  }

  .faction:hover {
    transform: translateY(-4px);
    box-shadow: 0 8px 16px rgba(0, 0, 0, 0.3);
  }

  /* Space for the faction's symbol */
  .symbol {
    flex: 1;
    display: flex;
    align-items: center;
    justify-content: center;
    width: 100%;
    font-size: 2.4rem;
  }

  .symbol img {
    max-width: 70%;
    max-height: 100%;
  }

  .faction-name {
    font-size: 1rem;
    line-height: 1.2;
  }

  .former-tag {
    display: block;
    font-size: 0.7rem;
    opacity: 0.8;
    letter-spacing: 0.08em;
  }

  /* Former factions appear slightly faded */
  .faction.former { filter: saturate(0.5) brightness(0.9); }
</style>

# Factions

The various forces which call the Heartlands home, or have a vested interest in its events.

<div class="faction-grid">
<a class="faction" style="--color:#00f0fc" href="factions/church-of-time"><div class="symbol">🔭</div><div class="faction-name">Church of Time</div></a>
<a class="faction" style="--color:#6e00c2" href="factions/keep-of-time"><div class="symbol">🧭</div><div class="faction-name">Keep of Time</div></a>
<a class="faction" style="--color:#012545" href="factions/breathing-moulde"><div class="symbol">⛭</div><div class="faction-name">Breathing Moulde</div></a>
<a class="faction" style="--color:#730103" href="factions/astral-court"><div class="symbol">⚖️</div><div class="faction-name">Astral Court</div></a>
<a class="faction" style="--color:#97b1c7" href="factions/penitents-of-the-timeless-wastes"><div class="symbol">❄️</div><div class="faction-name">Penitents of the Timeless Wastes</div></a>
<a class="faction" style="--color:#047502" href="factions/church-of-life"><div class="symbol">🐐</div><div class="faction-name">Church of Life</div></a>
<a class="faction" style="--color:#769942" href="factions/bard-board"><div class="symbol">🪉</div><div class="faction-name">Bard Board</div></a>
<a class="faction former" style="--color:#b9f21d" href="factions/elven-council"><div class="symbol">🌿</div><div class="faction-name">Elven Council<span class="former-tag">FORMER</span></div></a>
<a class="faction" style="--color:#ad5700" href="factions/penitents-of-the-lifeless-wastes"><div class="symbol">🌋</div><div class="faction-name">Penitents of the Lifeless Wastes</div></a>
<a class="faction" style="--color:#a8005d" href="factions/legions-of-silence"><div class="symbol">😈</div><div class="faction-name">Legions of Silence</div></a>
<a class="faction" style="--color:#63005a" href="factions/syndicates"><div class="symbol">🔫</div><div class="faction-name">Syndicates</div></a>
<a class="faction former" style="--color:#02cc78" href="factions/dewhelm-drug-ring"><div class="symbol">🧪</div><div class="faction-name">Dewhelm Drug Ring<span class="former-tag">FORMER</span></div></a>
<a class="faction former" style="--color:#36191a" href="factions/gourmands"><div class="symbol">😋</div><div class="faction-name">Gourmands<span class="former-tag">FORMER</span></div></a>
<a class="faction" style="--color:#015943" href="factions/stilldead"><div class="symbol">💀</div><div class="faction-name">Stilldead</div></a>
<a class="faction" style="--color:#2e2622" href="factions/slitherers"><div class="symbol">🐍</div><div class="faction-name">Slitherers</div></a>
<a class="faction" style="--color:#9bc1d4" href="factions/the-rothold"><div class="symbol">⚔️</div><div class="faction-name">The Rothold</div></a>
<a class="faction" style="--color:#998129" href="factions/donfair-empire"><div class="symbol">🏰</div><div class="faction-name">Donfair Empire</div></a>
<a class="faction" style="--color:#c40000" href="factions/court-of-princes"><div class="symbol">👑</div><div class="faction-name">Court of Princes</div></a>
<a class="faction" style="--color:#3e524f" href="factions/garnus-alliance"><div class="symbol">⛰️</div><div class="faction-name">Garnus Alliance</div></a>
<a class="faction" style="--color:#3d3d3d" href="factions/dwarves-of-ervein"><div class="symbol">⚒️</div><div class="faction-name">Dwarves of Ervein</div></a>
<a class="faction" style="--color:#a66100" href="factions/splintered-tavern"><div class="symbol">🍺</div><div class="faction-name">Splintered Tavern</div></a>
</div>
