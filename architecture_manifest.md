# FTL: Faster Than Light -- Architecture Manifest

**status:** research-integrated
**last_reconciled:** 2026-06-02
**research_run:** P1 ingested 2026-06-02 (deep-research cascade handoff); P2 ingested 2026-06-02 (deep-research cascade handoff)

This file serves as the corpus manifest. FTL is a procedural roguelike -- there is no fixed zone graph that can be pre-built, so `nav/` is not created. The star-map system (localization-mechanism class: map-system) handles spatial navigation in-game; nav questions are served by per-question lookup against `mechanics.md`, `sections/sector_types.md`, and the architecture summary below.

## Hintforge manifest

```
corpus-core-version: 6
game-version: "latest"
game-version-platform: "PC / Steam"
game-version-as-of: 2026-06-02
vector-extensions: crew, factions
```

## Vector extensions

- `crew/` -- role/species-aggregated crew entities (8 species). Indexed by `crew/index.md`; per-species files populated at P1.
- `factions/` -- alien races and faction behaviors (9 factions). Indexed by `factions/index.md`; per-faction files populated at P1.

## Game-type classification

- **Game-type label:** procedural -- 8 sectors/run, each a zone of 19-24 beacons placed randomly on a 6×4 grid; events drawn from sector-type pools; permadeath. [Confirmed: 5 sources]
- **Localization-mechanism class:** map-system (in-game star map; nav/ skipped)
- **Cross-system dependency density:** high
- **Named-NPC density:** low (npcs/ skipped)
- **Faction density:** medium (factions/ created)
- **Crew-system signal:** yes (crew/ created)
- **Reputation-system signal:** no (reputation/ skipped)

## Architecture Summary (P1)

### Sector type list (19)

48% green / 32% red / 20% purple on the map -- **color is misleading** (Zoltan green sectors are dangerous). Per-sector-type event notes: `sections/sector_types.md`.

| Canonical name | Slug | Window | Difficulty | AE-only |
|---|---|---|---|---|
| Civilian (Starting) Sector | civilian_starting | 1 only | Easy | No |
| Civilian Sector | civilian | 2-7 | Easy-Med | No |
| Engi Controlled Sector | engi_controlled | 2-7 | Easy | No |
| Engi Homeworlds | engi_homeworlds | 3+ (once) | Easy-Med | No |
| Zoltan Controlled Sector | zoltan_controlled | 2-7 | Hard | No |
| Zoltan Homeworlds | zoltan_homeworlds | 3+ (once) | Hard | No |
| Mantis Controlled Sector | mantis_controlled | 2-7 | Med-Hard | No |
| Mantis Homeworlds | mantis_homeworlds | 3+ (once) | Hard | No |
| Rock Controlled Sector | rock_controlled | 2-7 | Med | No |
| Rock Homeworlds | rock_homeworlds | 5+ (once) | Med-Hard | No |
| Pirate Controlled Sector | pirate_controlled | 2-7 | Med | No |
| Rebel Controlled Sector | rebel_controlled | 2-7 | Med | No |
| Rebel Stronghold | rebel_stronghold | 5+ (once) | Hard | No |
| Slug Controlled Nebula | slug_controlled_nebula | 4+ | Med-Hard | No |
| Slug Home Nebula | slug_home_nebula | 4+ (once) | Hard | No |
| Uncharted Nebula | uncharted_nebula | 2-7 | Med | No |
| Abandoned Sector | abandoned_sector | 2-7 | Med | **Yes** |
| Hidden Crystal Worlds | hidden_crystal_worlds | after Rock HW | Hard | No |
| The Last Stand | the_last_stand | 8 only | Hardest | No |

> **Naming correction:** there are NO separate "Lanius Controlled Sector" / "Lanius Homeworlds" event-pool types (the P1 brief named three). Lanius content reaches the player via the **Abandoned Sector** and Lanius enemy ships. The `sections/` scaffold's "Lanius Controlled/Homeworlds" row is superseded by this.

### Chapter ↔ zone mapping
- Sector 1: always Civilian (Starting). Sectors 2-7: random from green/red/purple pools with gating (Engi/Zoltan/Mantis HW at 3+; Rock HW & Rebel Stronghold at 5+; Slug nebulae at 4+; each unique type once/game). Sector 8: always The Last Stand. Hidden Crystal Worlds is off-map (via Ancient device in Rock Homeworlds).

### Zone graph
- **Rebel Fleet pursuit** advances ~one beacon-column per jump (datamined 0x40/jump); nebula visits slow it; mercenary/Distraction-Buoys delay it. Full math in `mechanics.md`.
- **Exit beacon:** always present/visible, opposite side from start; reaching it = story-gate to next sector. **No backtracking between sectors** (one-way). Run always ends at The Last Stand.

### DLC list
**No paid DLC.** Advanced Edition is a free, default-on update (toggleable). All AE content is in scope.

### Optional content registry
- Store beacons (1-jump-marked; AE often 2 pages), Distress beacons (some need blue-option keys), Asteroid/Nebula beacons (risk/reward), the Crystal sector unlock chain (missable -- `sections/missables.md`), and the Rebel Flagship's 3 phases (only in The Last Stand).

### Source-language set
- Founder country **corrected**: Subset Games was founded in **Shanghai, China** (Justin Ma & Matthew Davis, former 2K China staff), not Canada as the brief stated; working language English.
- Non-English sources used: **Japanese** (iphoneac.com, seesaawiki.jp/ftl, hatelabo.jp, game-pcs.com, gorakuhunter.com), **Russian** (StopGame.ru, gamin.me, ru.fandom.com, Steam RU guides).

### Achievement stub count
51 (Steam, added Jan 2020). All 51 resolved -- see `achievements.md`.

### Content categories
weapons (7 types, 40+), ammo/consumables (Missiles/Drone Parts/Fuel), upgrades (all systems), support items (drones + augments), builds (5+ archetypes), controls, settings present. crafting_materials and abilities absent.

## P2 Support Topology

_source: P2 deep-research cascade 2026-06-02 (ftl.fandom.com + Steam community + datamining + JP/RU sources) · capture: web_fetch · confidence: medium · category: mainline_

### Beacon type taxonomy (cross-sector reference)
`spoiler: none · enemy-tier: 0 · puzzle-tier: 0`

| Beacon type | Map appearance | Notes |
|---|---|---|
| Standard / unexplored | Plain dot | Most beacons; unknown until visited |
| Distress | Flashing icon, visible within 1 jump | Stays until overtaken; may be rescue/ambush/empty/special |
| Store | "STORE" grey border, visible within 1 jump | Repair, buy weapons/drones/augments/systems/crew |
| Exit | "EXIT" green border, visible from any distance | Transition to next sector |
| Quest | "QUEST" marker | Spawned by events; replaces non-store/exit/quest beacon |
| Nebula | Cloud indicator | Sensor blackout; Rebel slowdown |
| Rebel-captured | Two "!!" red circle | Forced Elite Fighter fight, often ASB; 1 fuel reward |
| Long-Ranged Scanners reveal | Yellow triangle "!" = ship present; orange hazard-stripe = hazard | Reveals adjacency only; "no ship" ≠ no forced fight |

`spoiler: late-game · enemy-tier: 0 · puzzle-tier: 0` — Federation Repair beacon (The Last Stand only): Repair icon; 15 hull + 22-44 scrap, 5 fuel, 4 missiles, 5 drone parts on first visit; reusable via Wait. [Confirmed: 4 sources]

### Sector traversal patterns (P2 extensions)

**Sector position windows (refinement of P1 table):**
`spoiler: none · enemy-tier: 0 · puzzle-tier: 0`
- `civilian_starting` always Sector 1; has fewer stores/items/quests/nebulas than recurring civilian sectors. [Confirmed]
- Recurring types (`civilian`, `engi_controlled`, `zoltan_controlled`, `mantis_controlled`, `rock_controlled`, `pirate_controlled`, `rebel_controlled`, `slug_controlled_nebula`, `uncharted_nebula`, `abandoned_sector`): no fixed position, can appear multiple times. [Confirmed]

`spoiler: progression · enemy-tier: 0 · puzzle-tier: 0`
- Homeworld variants (`engi_homeworlds`, `zoltan_homeworlds`, `mantis_homeworlds`, `slug_home_nebula`): once per game, Sector 3+. [Confirmed]
- `rock_homeworlds` and `rebel_stronghold`: once per game, Sector 5+. [Confirmed]

`spoiler: late-game · enemy-tier: 0 · puzzle-tier: 0`
- `hidden_crystal_worlds`: not on the map; reached via the Ancient device in Rock Homeworlds only. [Confirmed]
- `the_last_stand`: always Sector 8. [Confirmed]

**Rebel Fleet advance -- exact datamined mechanic (refinement of P1):**
`spoiler: none · enemy-tier: 0 · puzzle-tier: 0`
- Counter is a 4-byte signed integer initialized to **0xFFFFFC41 (−959)** at sector start; increases **+0x40 (64) per jump**. The negative starting value is the mechanical grace period. Frozen at 0x3C (60) in Sector 8. Uniform across all sector types -- only event modifiers change it. Treat "~1 beacon column per jump" as an observational description; the exact pixel-mapping is unconfirmed. [Single source -- verify · class: datamining forum (FearLess Cheat Engine)]

`spoiler: progression · enemy-tier: 0 · puzzle-tier: 0`
- **Rebel Controlled sectors** add one jump to the fleet advance on entry (a Rebel guard at the entrance beacon). [Confirmed]
> **Cross-system dependency** -- see `dependencies.md` DEP-009: Entering a Rebel Controlled sector adds +1 jump to the fleet advance counter, shortening the safe-beacon budget by one jump from sector entry.

**Exit beacon:**
`spoiler: none · enemy-tier: 0 · puzzle-tier: 0`
- Always exactly one per sector, visible from any distance, on the opposite side from sector entry. Reachable even if Rebels have overtaken it (triggers a powerful Rebel ship fight, often with ASB). [Confirmed]

`spoiler: late-game · enemy-tier: 0 · puzzle-tier: 0`
- The Last Stand has no exit beacon -- the goal is defending the Federation base until the Flagship is destroyed. [Confirmed]

**Safe beacon budget:**
`spoiler: progression · enemy-tier: 0 · puzzle-tier: 0`
- Community consensus: never beeline the exit; maximize beacons visited per sector, prioritizing un-overtaken beacons. A player can typically clear most of a 17-24 beacon sector. No single hard number; practical budget = "as many as you can reach before the red zone hits the exit column." Long-Ranged Scanners are the key tool to skip empty/ship-less beacons. [Confirmed: multiple community sources]

**Per-sector-type beacon distribution:**
`spoiler: none · enemy-tier: 0 · puzzle-tier: 0` — file-count approximations from game data; actual maps vary due to event-list overflow and generation variance. [Confirmed: wiki + Steam]

| Sector type | Stores | Hostile | Distress | Notable |
|---|---|---|---|---|
| Civilian / Starting | 2-3 | 6-8 | 1-2 | 2-4 neutral, 0-2 quests, 0-8 nebula |
| Engi Controlled | 2-3 | 5-7 | 1-3 (up to 4) | 5 items, 1 quest, 4-6 neutral |
| Zoltan Controlled | 2 | 6-8 | varies | 1-2 boarders, 2-6 nebula (dangerous) |
| Mantis Controlled | 1-2 | 6-7 | varies | 2-3 empty |
| Rock Controlled | 2 | 6-8 | varies | 7-8 neutral |
| Pirate / Rebel Controlled | 1-2 | 6-8 | varies | 0-5 nebula |
| Slug nebulae / Uncharted Nebula | 2-3 / 1-2 | varies | varies | Sensor blackout; ~0.8% Uncharted Nebula has 0 stores (gen bug) |
| Abandoned Sector (AE) | 2 | varies | varies | Lanius events |

Store richness ranking: Civilian/Engi/Slug best (2-3); Rock/Zoltan/Lanius middling (~2); Pirate/Rebel/Nebula/Mantis fewest (1-2). [Confirmed]

**Navigation hazards (P2 detail, extends P1 sector notes):**
`spoiler: none · enemy-tier: 0 · puzzle-tier: 0`
- **Nebula beacons (any sector):** 50% Rebel slowdown when visited from a non-nebula sector; 20% slowdown inside a nebula sector. Some carry plasma/ion storms (halves reactor capacity). Sensors disabled in nebula sectors entirely. [Confirmed]
- **Asteroid fields:** periodic asteroid hits knock down one shield layer or deal 1 hull/system damage; frequency scales with shield count; 2+ shield layers strongly recommended. [Confirmed]
- **Pulsars (AE only):** ion pulse every 11-18s (5s warning); ionizes 2 systems per ship; shields hit first; damage = 1 + 0.5×(system power) rounded down. Reverse Ion Field is the only counter. [Confirmed: wiki]
- **Solar flares / Red giants:** fire every 28-34s (5s warning). [Confirmed: wiki]
- **Anti-Ship Battery (ASB):** 3 hull damage + guaranteed breach; dodgeable via cloak, high evasion, or jumping before it fires; never at exit beacons on Easy. [Confirmed]
- **IN DANGER status:** asteroid/pulsar/solar-flare/ASB environments impose this; prevents ship-menu upgrades while active. [Confirmed: wiki]

### Auto-save mechanics
`spoiler: none · enemy-tier: 0 · puzzle-tier: 0`

- FTL writes to `continue.sav` (run state) and `ae_prof.sav` (profile/achievements) at least once per location. Single rolling slot -- menu shows only "Continue," no manual save or multi-slot system. Captures full ship/crew/inventory/event/map state. [Confirmed: 5 sources]
- **On death:** `continue.sav` is deleted (permadeath by design). [Confirmed]
- **Known loss case:** closing the game via OS without using "Save & Quit" can lose the current-location update. Save files live at `My Documents\My Games\FasterThanLight\`; antivirus "ransomware protection" can block writes. [Confirmed: community]
- **Save-scumming:** the design intends iron-man play; copying `continue.sav` before a risky encounter and restoring it is technically possible but considered poor form by the roguelike community. External tools (synogen/ftlautosave, Nexus FTLAutosave) automate snapshots. [Confirmed: 5 sources] [Single source on exact tool names -- verify]

### Store topology
`spoiler: none · enemy-tier: 0 · puzzle-tier: 0`

- Every sector has ≥1 guaranteed store. Inventory is **fixed on sector generation** -- the store's contents are saved on first visit and do not change on return. [Confirmed: wiki datamining + Steam]
- Each store has category slots (weapons, drones, augments, systems, crew); each slot shows 3 random items. Rules: never sells duplicate weapons/drones/augments; if ship has <11 systems+subsystems, 50% chance first slot is forced to systems; buying a medical system replaces the existing one; Teleporter always installs as 2-tile. [Confirmed]
- Resource prices (fuel/missiles/drone-parts) are fixed; hull-repair price scales with sector number. [Confirmed]
- **Reload caveats:** reloading at any store re-rolls crew skills and forces Drone Control to stock a Defense Drone Mk I; event-spawned stores vanish on reload; boarders-present makes the store disappear on exit. [Confirmed: wiki datamining]

`spoiler: late-game · enemy-tier: 0 · puzzle-tier: 0`
- The Last Stand has 1 store beacon (often overtaken); Hidden Crystal Worlds has no store-opening events (only Crystal weapons/crew sold at its own beacon). [Confirmed]

### Distress beacon patterns
`spoiler: none · enemy-tier: 0 · puzzle-tier: 0`

- Distress beacons draw from the DISTRESS event list plus distress-tagged events in other lists (an Engi sector's "1-3 distress" cap can be exceeded in practice). Outcomes: rescue (crew/scrap/resources), ambush, trade, or nothing -- all weighted per-event; no global percentage exists. [Confirmed: wiki + Steam]
- Some outcomes are affected by crew species via blue options (e.g., Rock Plating / Crew Teleporter on asteroid-belt distress; Engi/Rock crew on mining colony). [Confirmed]
- Sector-type-specific event pools exist (`DISTRESS_BEACON_ENGI`, `DISTRESS_BEACON_PIRATE`, etc.). [Confirmed: wiki]
- Out-of-fuel "Wait" event: ~40% nothing-chance with the distress beacon off; activating the distress beacon greatly raises encounter and rescue chance. [Confirmed: community]

### Fast-travel and hub-and-spoke
`spoiler: none · enemy-tier: 0 · puzzle-tier: 0`

- **No fast-travel.** All movement is adjacent-beacon jumps (1 fuel + FTL drive + manned Piloting). No augmentation or event grants a non-adjacent jump within a sector. Long-Ranged Scanners only *reveal* adjacent beacons; they do not extend jump range. [Confirmed]
- **No hub-and-spoke.** Sector transition is one-way (Exit beacon to next sector); previous sectors cannot be revisited in the same run. Re-jumping to a beacon within the current sector is possible (1 fuel; enemy ships respawn at restored HP) but you cannot go back to a prior sector. [Confirmed]

`spoiler: late-game · enemy-tier: 0 · puzzle-tier: 0`
- **Crystal sector exception:** on exit from the Hidden Crystal Worlds you are teleported directly to a random sector following the Rock Homeworlds number -- no sector choice. [Confirmed]

## Sources

- ftl.fandom.com (Sectors, Rebel Fleet, Crystal Cruiser, ship pages, Blue Options, Beacons, Stores, Ancestry, Ancient device, Zoltan research facility) -- community-wiki, captured via P1/P2 cascade 2026-06-02
- Japanese & Russian community sources (see above); Giant Bomb (dev-origin correction); Destructoid/Steam Hunters (51-achievement count); FearLess Cheat Engine datamining
- Steam Community guides (save mechanics, Blue Events, store discussions); GitHub synogen/ftlautosave; Subset Games Forum (Rebel fleet speed thread)
