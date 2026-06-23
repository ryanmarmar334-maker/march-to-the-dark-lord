# The March to the Dark Lord

A party-based tactics roguelite playable entirely in your browser — no install, no build step, no dependencies. Just open the HTML file and play.

## Play it

Download `The_March_to_the_Dark_Lord.html` and open it in any modern browser. That's it.

## What it is

You forge a company of four heroes and descend through nine themed areas in random order. The tenth gate is always the Dark Lord's formation. Win or lose, each run is different.

The whole game is **set a status, then cash it in.** Stack Burn on a target, then Combust it for triple damage ignoring armour. Build Bleed on a foe that likes to move, then Rupture it. Freeze a unit solid with Chill, then pile on while it loses its turn. Every class is built around one half of that loop — the setup or the payoff — and the party has to combine them.

## Features

- **Four classes** — Fighter, Rogue, Wizard, Cleric — each with basic and committed-tier skills ranked R1–R5
- **Six statuses** — Burn, Bleed, Poison, Chill/Freeze, Sunder, Stun — with distinct rules and detonation combos
- **Ten areas**, nine of which appear in random order each run, each with a skirmish and a boss that tests a specific strategy
- **Gear system** — weapons, armour, shields, and focus items with VIT/STR gates; Pierce mechanic on heavy weapons
- **Glyphs** — socketed enchantments that scale with their own rarity (common → artifact)
- **Professions** — Alchemy, Trader, Blacksmithing — ranked alongside skills
- **Loot, shops, leveling** — pick 3 of 5 drops after each fight; buy and sell between areas; spend stat and skill points after every boss
- **Three difficulty modes** — Easy (round undo), Normal (revive at half HP), Hard (permadeath + skill points cost stat points)
- **Meta unlocks** — Dwarf race and Bard class unlock across runs on Normal/Hard

## How to play

**Party phase → Enemy phase, repeat.**

Select a hero, choose an action from the bar at the bottom, tap a target on the board. Each hero has an Energy budget per round (roughly DEX ÷ 5). Moving costs 1 energy. Attacks cost their weapon's listed energy — light weapons' first swing each round is free. Skills cost what the pill shows.

When you're done with all your heroes, press **End Turn** and the foes move.

**Armour soak** (the 🛡 number) refreshes each round and absorbs damage before HP. It's spent as hits land, so burst damage from multiple attacks strips it fast. Heavy weapons **Pierce** — their base damage bypasses soak entirely. Magic and damage-over-time also ignore soak.

The in-game **How to Play** covers all six statuses and gear rules across four pages.

## Classes at a glance

| Class | Stats | Set skill | Role |
|---|---|---|---|
| Fighter | STR + VIT | Bash | Frontline; stuns, sunders, guards allies |
| Rogue | DEX + LCK | Poisoned Throw | Applies poison and bleed from range; detonates with Rupture |
| Wizard | FOC + LCK | Magic Bolt | Ranged spells; applies Burn and Chill; detonates with Combustion |
| Cleric | VIT + FOC | Mend | Heals, cleanses poison, blesses allies for bonus damage |

## The ten areas

Nine of these ten appear each run in random order, then the Dark Lord always closes at area 10.

| Area | Boss threat | What it tests |
|---|---|---|
| The Forest | Scarred Bear | Burst damage and tankiness |
| Goblin Burrowers | Goblin King | Add-flood at 50% HP |
| The Swamp | Bog Witch | Protected priority target |
| The Graveyard | Necromancer | Anti-sustain focus fire |
| The Caverns | Broodmother | Summoner swarm race |
| Frostpeak | Frost Wyrm | Chill/freeze control |
| The King's Road | Black Knight | Armour wall + ranged triangle |
| Trollbridge | Bridge Troll | Regen race — Burn stops it |
| The Fungal Deep | Myconid Sovereign | Attrition and cleansing |
| Harpy Cliffs | The Matriarch | Reach and closing the gap |

## Roadmap

- [ ] Bard class (meta unlock is flagged; class not yet built)
- [ ] Conjurer class
- [ ] Multi-encounter areas instead of single skirmish + boss
- [ ] In-run save / continue
- [ ] Book and Censer focus items as loot drops
- [ ] Alchemy crafting UI
- [ ] Telegraphed Dark Lord ultimate (wind-up + mechanical phase shift)
- [ ] Specialist tier skills (rank 31+)
- [ ] Node test harness + Playwright UI smoke test

## Technical notes

Single file: HTML + CSS + JS, vanilla, no frameworks. Google Fonts loaded by URL (degrades gracefully offline). Meta unlocks persist via `localStorage` with an in-memory fallback.

To syntax-check without a browser: extract the `<script>` body and run `node --check`.

---

*Original design and code produced collaboratively. No third-party assets bundled.*
