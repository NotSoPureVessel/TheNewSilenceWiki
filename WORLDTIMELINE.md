---
title: World Timeline
---

<style>
  .timeline {
    --line: #444;
    position: relative;
    max-width: 960px;
    margin: 2rem auto;
    padding: 0 1rem;
  }

  /* The single line down the middle */
  .timeline::before {
    content: "";
    position: absolute;
    top: 0;
    bottom: 0;
    left: 50%;
    width: 4px;
    margin-left: -2px;
    background: var(--line);
    z-index: 1;
  }

  /* Large colored era boxes */
  .era {
    position: relative;
    margin: 0 0 2.5rem;
    padding: 1.5rem 1rem 1rem;
    border-radius: 14px;
    border: 2px solid rgba(0, 0, 0, 0.15);
    background: var(--era-color);
  }

  .era-title {
    position: relative;
    z-index: 3;
    width: fit-content;
    margin: 0 auto 1.5rem;
    padding: 0.4rem 1.2rem;
    background: #222;
    color: #fff;
    border-radius: 999px;
    font-size: 1.25rem;
    font-weight: 700;
    text-align: center;
  }

  .era-dates {
    display: block;
    font-size: 0.8rem;
    font-weight: 400;
    opacity: 0.8;
  }

  /* One row = label (left) | line | details (right) */
  .entry {
    position: relative;
    z-index: 2;
    display: grid;
    grid-template-columns: 1fr 1fr;
    column-gap: 2.5rem;
    row-gap: 0.7rem;
    margin-bottom: 1.5rem;
  }

  .entry .label {
    grid-column: 1
    text-align: right;
    font-weight: 700;
    font-size: 1.1rem;
    color: #1a1a1a;
  }

  .entry .label small {
    display: block;
    font-weight: 400;
    font-style: italic;
  }

  .entry .details::before {
  content: "–";
  position: absolute;
  left: 0;
  top: 0;
  }
  
  .entry .details {
    grid-column: 2;
    position: relative;
    padding-left: 1.2em;
    text-align: left;
    color: #1a1a1a;
    line-height: 1.45;
  }

  /* Dot on the line for each entry */
  .entry::after {
    content: "";
    position: absolute;
    top: 0.45rem;
    left: 50%;
    width: 14px;
    height: 14px;
    margin-left: -7px;
    background: #fff;
    border: 3px solid var(--line);
    border-radius: 50%;
  }

  /* Era colors – change these freely */
  .era-mythology  { --era-color: #e9d8fd; }
  .era-conquest   { --era-color: #fed7d7; }
  .era-faith      { --era-color: #fefcbf; }
  .era-revolution { --era-color: #c6f6d5; }

  @media (max-width: 600px) {
    .entry { column-gap: 1.6rem; font-size: 0.9rem; }
    .era-title { font-size: 1rem; }
  }
</style>

# Timeline

<div class="timeline">

<div class="era era-mythology">
<div class="era-title">Age of Mythology<span class="era-dates">c. 3000 – 1200 BCE</span></div>
<div class="entry">
<div class="label">c. Fae Mythology</div>
<div class="details">It is said the Fae were among the first beings to evolve to the state we know them in now.</div>
<div class="details">Among these immortal eldritch Fae, Ogrimmal ascended to godhood.</div>
<div class="details">He and his kin departed the Heartlands to the Feywild to allow other life in the Heartlands to grow naturally and outside their influence for as long as possible.</div>
<div class="details">Eventually one of Ogrimmal’s own kin named Vishkaz challenged him for his divine throne
</div>
<div class="details">The corpse of this usurper Fae fell to the earth, its blood mixing with Ogrimmal’s own blood and tears, from which sprouted Faefall.</div>
<div class="details">Ogrimmal guided the life that was born there, and thus the first mortal Fae including elves and hobgoblins were born.</div>
</div>
<div class="entry">
<div class="label">The Age of Heroes<small>sub-era</small></div>
<div class="details">Legendary figures and epic tales shape the cultural memory of the region.</div>
</div>
<div class="entry">
<div class="label">c. 1250 BCE</div>
<div class="details">A legendary war between two great cities becomes the foundation of a famous epic.</div>
</div>
</div>

<div class="era era-conquest">
<div class="era-title">Age of Conquest<span class="era-dates">c. 800 BCE – 100 CE</span></div>
<div class="entry">
<div class="label">Fae Mythology</div>
<div class="details">The first recorded athletic games unite rival city-states in shared competition.</div>
</div>
<div class="entry">
<div class="label">The Rise of Empires<small>sub-era</small></div>
<div class="details">Powerful rulers expand their borders through military campaigns and alliances.</div>
</div>
<div class="entry">
<div class="label">323 BCE</div>
<div class="details">The death of a famed conqueror splits his vast empire among rival generals.</div>
</div>
</div>

<div class="era era-faith">
<div class="era-title">Age of Faith<span class="era-dates">c. 100 – 1500 CE</span></div>
<div class="entry">
<div class="label">476 CE</div>
<div class="details">Imperial authority collapses in the west, and religious institutions become the main source of stability.</div>
</div>
<div class="entry">
<div class="label">The Crusades<small>sub-era</small></div>
<div class="details">Successive military expeditions reshape trade, politics, and religious relations.</div>
</div>
</div>

<div class="era era-revolution">
<div class="era-title">Age of Revolution<span class="era-dates">c. 1500 – 1900 CE</span></div>
<div class="entry">
<div class="label">1776</div>
<div class="details">Colonists declare independence, inspiring movements for self-rule worldwide.</div>
</div>
<div class="entry">
<div class="label">1789</div>
<div class="details">Revolution in France overturns the monarchy and spreads new ideas of citizenship.</div>
</div>
</div>

</div>
