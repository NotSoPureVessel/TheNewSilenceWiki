---
title: World Timeline
---

<style>

  html { overflow-x: hidden; }
  
  .timeline {
    --line: #444;
    --line-x: 30%;
    position: relative;
    max-width: 960px;
    margin: 2rem auto;
    padding: 0;
  }

  /* The single line down the middle */
  .timeline::before {
    content: "";
    position: absolute;
    top: 0;
    bottom: 0;
    left: var(--line-x);
    width: 4px;
    margin-left: -2px;
    background: var(--line);
    z-index: 1;
  }

  .era::before {                 /* NEW: the full-width colored box */
    content: "";
    position: absolute;
    top: 0;
    bottom: 0;
    left: 50%;
    width: 100vw;
    margin-left: -50vw;
    background: var(--era-color);
    border-top: 2px solid rgba(0, 0, 0, 0.15);
    border-bottom: 2px solid rgba(0, 0, 0, 0.15);
    z-index: 0;
  }
  
  /* Large colored era boxes */
  .era {
    position: relative;
    margin: 0 0 2.5rem;
    padding: 1.5rem 0 1rem;
  }

  .era-title {
    position: relative;
    z-index: 3;
    width: calc(var(--line-x) * 2);   /* centers the text on the line */
    margin: 0rem 0 1.5rem;         /* position relative to the rest of the era box */
    padding: 0.8rem 0;
    background: #000;
    color: #fff;
    font-size: 1.25rem;
    font-weight: 700;
    text-align: center;
    box-shadow: 0 0 0 100vmax #000;   /* stretches the black out to the edges of the page */
    clip-path: inset(0 -100vmax);     /* keeps the stretch horizontal only */
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
    grid-template-columns: calc(var(--line-x) - 1.25rem) 1fr;
    column-gap: 2.5rem;
    row-gap: 0.7rem;
    margin-bottom: 1.5rem;
  }

  .entry .label {
    grid-column: 1;
    text-align: right;
    font-weight: 700;
    font-size: 1.1rem;
    color: #1a1a1a;
  }

  .entry .label   { padding-left: 1rem; }   /* NEW: add to your existing label rule */
  .entry .details { padding-right: 1rem; }  /* NEW: add to your existing details rule */

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
    left: var(--line-x);
    width: 14px;
    height: 14px;
    margin-left: -7px;
    background: #fff;
    border: 3px solid var(--line);
    border-radius: 50%;
  }

  /* Era colors – change these freely */
  .era-mythology        { --era-color: #e9d8fd; }
  .era-conquest         { --era-color: #fc9c60; }
  .era-abundance-1      { --era-color: #c6f6d5; } 
  .era-hunt             { --era-color: #fefcbf; }
  .era-abundance-2      { --era-color: #c6f6d5; }
  .era-screams          { --era-color: #ff5959; }
  .era-grey             { --era-color: #a8a8a8; }

  @media (max-width: 600px) {
    .entry { column-gap: 1.6rem; font-size: 0.9rem; }
    .era-title { font-size: 1rem; }
  }
</style>

# Timeline
An overview of Heartlands history, compiled by the Keep of Time.

<div class="timeline">

<div class="era era-mythology">
<div class="era-title">Age of Mythology<span class="era-dates"> The time before recorded history, detailing the fabled origin of lands and peoples </span></div>
<div class="entry">
  <div class="label">Fae Mythology</div>
    <div class="details">It is said the Fae were among the first beings to evolve to the state we know them in now.</div>
    <div class="details">Among these immortal eldritch Fae, Ogrimmal ascended to godhood.</div>
    <div class="details">He and his kin departed the Heartlands to the Feywild to allow other life in the Heartlands to grow naturally and outside their influence for as long as possible.</div>
    <div class="details">Eventually one of Ogrimmal’s own kin named Vishkaz challenged him for his divine throne</div>
    <div class="details">The corpse of this usurper Fae fell to the earth, its blood mixing with Ogrimmal’s own blood and tears, from which sprouted Faefall.</div>
    <div class="details">Ogrimmal guided the life that was born there, and thus the first mortal Fae including elves and hobgoblins were born.</div>
</div>

<div class="entry">
  <div class="label">Dwarven Mythology</div>
    <div class="details">The earth itself trembled and gave birth to life, the dwarves.</div>
    <div class="details">This life was guided by the hand of Ogrimmal, who acted as a foster father to the dwarven people.</div>
    <div class="details">Theos taught the Dwarven people to understand their origins.</div>
    <div class="details">These children of three immortal parents revere the Earth most of all, but are also artisans and engineers.</div>
    <div class="details">They believe everything taken from the earth must be treated with respect, and work in their forges to fashion into the most beautiful, powerful shape possible.</div>
</div>

<div class="entry">
  <div class="label">Draconic Mythology</div>
    <div class="details">The lore of the dragons and dragonborn are a closely guarded secret even among their own race.</div>
    <div class="details">They swear fealty to no order in the Heartlands divine or otherwise, serving only their personal desires.</div>
</div>

<div class="entry">
  <div class="label">Fell Mythology</div>
    <div class="details">Before all things, there was only the Silence, out of which the planes of existence were born.</div>
    <div class="details">There are those who would wish to return all of existence to that Silence.</div>
    <div class="details">Theos taught the Dwarven people to understand their origins.</div>
    <div class="details">The Fell Serpent, God of Silence, arose from this wish to undo all that has been done.</div>
    <div class="details">Those touched by feel blood and their descendants become Tieflings.</div>
</div>
</div>

<div class="era era-conquest">
  <div class="era-title">Age of Conquest<span class="era-dates">Year 0 - Year 34</span></div>  
  <div class="entry">
  <div class="label">Year 0</div>
    <div class="details">A hobbit named Barrabas Kane sets out to unite the scattered fiefdoms in the plains.</div>
    <div class="details">He declares himself first king, and names the plains under his control Donfair.</div>
  </div>

  <div class="entry">
  <div class="label">Year 8</div>
    <div class="details">Dissenters to Barrabas’ unification efforts rise up against him.</div>
    <div class="details">They are defeated and mostly executed, those who escape flee to Endormir and group up with Dwarven separatists.</div>
  </div>

  <div class="entry">
  <div class="label">Year 9</div>
    <div class="details">In pursuit of the rebels, the short-lived species of Donfair make contact with the Dwarves for the first time.</div>
  </div>

  <div class="entry">
  <div class="label">Year 11</div>
    <div class="details">After years of negotiation, Endormir and Donfair set out to unite their kingdoms and destroy all opposition.</div>
    <div class="details">It is said as the conquest march began, Theos watched in silence and Ogrimmal wept.</div>
  </div>

  <div class="entry">
  <div class="label">Year 34</div>
    <div class="details">The conquest is made complete. Barrabas Kane and the current Dwarven queen agree to pardon all dissenters who submit to their rule. Those who agree go on to found Hell’s Kitchen and the Rothold.</div>
  </div>
</div>

<div class="era era-abundance-1">
  <div class="era-title">First Age of Abundance<span class="era-dates">Year 34 - Year 229</span></div>  

  <div class="entry">
  <div class="label">Year 34</div>
    <div class="details">The conquest of Garnus and Donfair comes to an ends.</div>
  </div>

  <div class="entry">
  <div class="label">Year 130</div>
    <div class="details">On the epoch of his 14th decade in rule, Barrabas Kane passes away and leaves his eldest child to be king, founding the first royal family of Donfair.</div>
    <div class="details">His rule after the great conquest is remembered as a time of unprecedented peace.</div>
  </div>

  <div class="entry">
  <div class="label">Year 144</div>
    <div class="details">A gnome named Galliard Timbers sacrifices his many centuries of life to receive revelations from Theos.</div>
    <div class="details">He becomes known as the first Artificer.</div>
  </div>

  <div class="entry">
  <div class="label">Year 162</div>
    <div class="details">Thanks to leaps in technology, sea travel has become more safe.</div>
    <div class="details">Official studies of the arcane arts have begun.</div>
  </div>

  <div class="entry">
  <div class="label">Year 179</div>
    <div class="details">A wizard makes first recorded contact with another plane of existence, one even older than the Heartlands, and succumbs to madness. This wizard becomes the first warlock, a demigod of Silence now known as the Ferryman.</div>
    <div class="details">This place is dubbed the Silent Plane, the Shadowfell.</div>
  </div>

  <div class="entry">
  <div class="label">Year 183</div>
    <div class="details">First contact is made between Fae creatures and the rest of the world.</div>
    <div class="details">There are several border incidents, but eventually a truce that isolates the Faefall forest is made.</div>
  </div>

  <div class="entry">
  <div class="label">Year 225</div>
    <div class="details">Galliard Timbers receives a final revelation from Theos on his deathbed.</div>
    <div class="details">He uses the information in this revelation to draft a prototype invention and dubs it the Warforged, entrusting a piece of the blueprint to several lords in Donfair and Endormir.</div>
  </div>

  <div class="entry">
  <div class="label">Year 229</div>
    <div class="details">A Hobgoblin child receives a revelation from Theos.</div>
  </div>
</div>

<div class="era era-hunt">
  <div class="era-title">Age of the Hunt<span class="era-dates">Year 229 - Year 259</span></div>  

  <div class="entry">
  <div class="label">Year 229</div>
    <div class="details">A hobgoblin child receives a revelation from Theos, a vision of the world in flames and dragons overhead.</div>
    <div class="details">That night, a dragon descends upon Faefall and scorches much of it.</div>
    <div class="details">For the first time, the elven council of Dewhelm willingly reaches out to the rest of the world for aid.</div>
  </div>

  <div class="entry">
  <div class="label">Year 230</div>
    <div class="details">A gnome named Galliard Timbers sacrifices his many centuries of life to receive revelations from Theos.</div>
    <div class="details">He becomes known as the first Artificer.</div>
  </div>

  <div class="entry">
  <div class="label">Year 230</div>
    <div class="details">A pact is made across all nations to hunt the dragons to extinction.</div>
  </div>

  <div class="entry">
  <div class="label">Year 234</div>
    <div class="details">The first Warforged are birthed to fight the Dragons, with an urge to hunt and slay them programmed into them at the kernel level.</div>
  </div>

  <div class="entry">
  <div class="label">Year 259</div>
    <div class="details">The hunt is declared a victory, with the revelation of the world in flames averted.</div>
    <div class="details">Dragons who cooperated are granted amnesty and mostly retreat to hidden lairs, although some integrate into society and dragonborn become somewhat commonplace.</div>
    <div class="details">Connection and cooperation between nations, races, and cultures in the Heartlands reaches an all-time high.</div>
  </div>
</div>

<div class="era era-abundance-2">
  <div class="era-title">Second Age of Abundance<span class="era-dates">Year 259 - Year 337</span></div>  
  <div class="entry">
  <div class="label">Year 259</div>
    <div class="details">The struggle against Dragons is declared over.</div>
  </div>

  <div class="entry">
  <div class="label">Year 263</div>
    <div class="details">Reconstruction in the wake of the Draconic Hunt reaches an end, and society begins advancing beyond where they were the hunt began.</div>
    <div class="details">Cultural diaspora and intermingling reaches even Dewhelm, including the religion of Theos.</div>
  </div>

  <div class="entry">
  <div class="label">Year 264</div>
    <div class="details">For the first time, Non-Fae creatures witness the descent of Ogrimmal in Dewhelm’s annual summer solstice festival.</div>
    <div class="details">The college of Umbrage is established to bridge Faefall and Donfair.</div>
  </div>

  <div class="entry">
  <div class="label">Year 277</div>
    <div class="details">The Arcane Arts and Artificing have become part of everyday life in the world.</div>
  </div>

  <div class="entry">
  <div class="label">Year 293</div>
    <div class="details">In the timeless wastes, a dwarf follower of Ogrimmal creates the Jerboas, a species capable of surviving in the Dunes of Steel.</div>
    <div class="details">This draws the attention of Orimmal, and the dwarf becomes a demigod of life now known as Papa Sand.</div>
  </div>

  <div class="entry">
  <div class="label">Year 317</div>
    <div class="details">Trade Routes between kingdoms are now well established, and teleportation magic is being put into place.</div>
    <div class="details">The first splintered tavern is built and is overseen by Papa Sand.</div>
  </div>

  <div class="entry">
  <div class="label">Year 337</div>
    <div class="details">The High Council of the elves convenes to determine whether the faith of Theos should be allowed into their doctrine.</div>
  </div>
</div>

<div class="era era-screams">
  <div class="era-title">Century of Screams<span class="era-dates">Year 337 - Year 423</span></div>  

  <div class="entry">
  <div class="label">Year 337</div>
    <div class="details">The High Council of the elves is slaughtered in their own meeting chamber.</div>
    <div class="details">A war breaks out between the penitents of time and life over the slaughter.</div>
  </div>

  <div class="entry">
  <div class="label">Year 421</div>
    <div class="details">The Fell Serpent descends upon the heartlands, ending the war and beginning the Infernal Battle.</div>
  </div>

  <div class="entry">
  <div class="label">Year 422</div>
    <div class="details">The royal family of Donfair is overturned by the mercenary Rowl.</div>
    <div class="details">He is an ingenious general and steps up as the leader the world needs, but is simultaneously unstable and takes many concubines.</div>
  </div>

  <div class="entry">
  <div class="label">Year 423</div>
    <div class="details">The Fell serpent is finally slain on the west coast, and the Century of Screams comes to a close.</div>
  </div>
</div>

<div class="era era-grey">
  <div class="era-title">Age of the Grey<span class="era-dates">Year 423 - Year 450</span></div>  
  <div class="entry">
  <div class="label">Year 423</div>
    <div class="details">The Fell serpent is finally slain, marking the end Century of Screams.</div>
    <div class="details">Those touched by the serpent’s blood either by physically or by descendance were irreversibly and became Tieflings. The city of Pintor on the west coast is most deeply affected, and becomes known as Hell's Kitchen.</div>
  </div>

  <div class="entry">
  <div class="label">Year 425</div>
    <div class="details">Hidden within Donfair the Concubine Wars break out between Rowl’s children and their mothers, all vying to become his legitimate heir.</div>
    <div class="details">Most of Rowl’s children are killed in the invisible conflict, Gaius and Flora survive.</div>
  </div>

  <div class="entry">
  <div class="label">Year 428</div>
    <div class="details">Rowl is assassinated by his living children and concubines.</div>
    <div class="details">The Court of Princes is formed from Rowl's survivng children and becomes the new ruling body of Donfair. They initiate a search for any other living heirs.</div>
  </div>

  <div class="entry">
  <div class="label">Year 449</div>
    <div class="details">A second continent is discovered by a small expedition team, dubbed the New World.</div>
  </div>

  <div class="entry">
  <div class="label">Year 450</div>
    <div class="details">An order was sent out by both churches to assemble a new pilgrim force to explore this new world.</div>
  </div>
</div>

</div>
