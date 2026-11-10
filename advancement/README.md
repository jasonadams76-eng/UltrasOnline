# Advancement data
* `powers.json`, `talents.json` — what an official player may buy. `"double": true` = costs twice as much (the * items in the rule book). Edit freely; the Worker reads these files from the live site.
* `heroes_base.json` — the six heroes' original stats/powers/talents. The Worker uses it to price upgrades. It must match `PREMADE_HEROES` in index.html (the test suite checks this); if you change a hero's base sheet, regenerate it.
Costs: raise a stat or power rank one step = 100 x the new rank number (cap Monstrous 75). Talent 2000, power 4000 (starts at Typical 6); doubled for * items.
