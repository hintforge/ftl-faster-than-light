# Crystal

**entity-id:** crystal
**class:** crew
**entity-status:** unspecified
**entity-hidden:** no
**first-encounter-zone:** hidden_crystal_worlds
**status:** research-integrated
**last_reconciled:** 2026-06-02

## Current status
Rare ancestor species; tanky with a unique room-lockdown power. Recruitable **only** through a multi-step missable event chain (or pre-installed on the Rock Cruiser Type C). Gated content.

## Capabilities
- HP 125 · Move 0.5× (slowest, tied with Rock) · Combat 1.0× · Repair 1.0×.
- Trait: **Lockdown power** -- seals the room it's in (and everyone inside) behind crystal for ~10s, on a cooldown; takes **0.5× suffocation damage.** Dying-animation time 2s.
- Crystal Vengeance augment (10% chance to fire a shard back when hit; triggers "Sweet Revenge") is the Crystal ship-specific augment.
- Crystal weapons (Crystal Burst I/II, Heavy Crystal I/II) pierce 1 shield and are sold only in the Hidden Crystal Worlds -- see `items/weapons.md`.
- _source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com Crystal Cruiser page + datamining) · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_ — stats are visible once recruited. [Confirmed: datamining]

## Recruitment / Access -- the Crystal Cruiser unlock chain (missable)

> `spoiler: late-game` · enemy-tier 2 · puzzle-tier 1. The game's most complex missable sequence; required for the **Ancestry** achievement (when flown in the Rock Cruiser). Each step is `missable: yes`. Also indexed in `sections/missables.md`.

### Step 1 -- Damaged Stasis Pod
Event: "Dense asteroid field distress call" at a **distress beacon** in `pirate_controlled`, `engi_controlled`, `engi_homeworlds`, `rock_controlled`, or `rock_homeworlds`.
- Blue option (Rock Plating): "Make a thorough search of the area... without fear of stray asteroids" → **100% success**, Damaged Stasis Pod awarded.
- Without Rock Plating: "Search for the ship" → ~1/3 success (engine-dependent; failure deals hull damage).
- Occurrence chance: ~60% in Engi, ~69% in Pirate, ~75% in Rock sectors. [Confirmed: wiki datamining]
- **Reward:** Damaged Stasis Pod augment (no function until repaired at Zoltan facility).
- `missable: yes` — latest safe: Sector 3; the event becomes impossible to complete the chain from once Rock Homeworlds appears.

### Step 2 -- Zoltan Research Facility (datafile: ZOLTAN_CREW_STUDY)
Event at a **normal beacon** in `engi_controlled`, `engi_homeworlds`, `zoltan_controlled`, or `zoltan_homeworlds`. **Cannot occur in Rock Homeworlds.**
- Blue option (Damaged Stasis Pod): "Ask if they can fix this." → per FTL Fandom Wiki: *"You receive a Crystal crewmember named Ruwen and a quest marker will appear in the Rock Homeworlds (as long as Ruwen stays alive)."*
- Any Engi sector can host **both** Step 1 (as a distress beacon) and Step 2 (as a normal beacon) -- they use different event triggers.
> **Cross-system dependency** -- see `../dependencies.md` SEQ-002: Both Crystal chain prerequisites can be completed within Engi space; Step 1 appears at distress beacons, Step 2 at normal beacons (different pools).
- `missable: yes` — must occur before reaching Rock Homeworlds.

### Step 3 -- Ancient Device (Crystal sector unlock)
Event at a **normal beacon** in `rock_homeworlds` only (once per game, sector 5+).
- With Crystal crew (Ruwen or any Crystal): the beacon turns into a Quest beacon. Per FTL Fandom Wiki: *"Any Crystal crewmember can be used for the blue option, however, only the Crystal Crew from the Stasis Pod (Ruwen) will mark the entry beacon as a quest in the Rock Homeworlds sector."*
- Blue option (Crystal crew): "Reactivate it" → teleports to Hidden Crystal Worlds.
- `missable: yes` — Rock Homeworlds is once per game (Sector 5+); if it appears before Steps 1-2 are complete, the chain cannot be finished in this run.

### Step 4 -- Hidden Crystal Worlds
Reached via the quest marker (not on the star map). Rebels still pursue; enemy strength scales to the Rock Homeworlds sector number.
- Final quest beacon rewards: **Crystal Cruiser unlocked** (permanent); Crystal Vengeance augment; medium fuel + scrap; 10 hull repairs.
- Only Crystal weapons and Crystal crew are sold/recruitable here.
- On exit: no sector choice -- teleported to a random sector immediately following the Rock Homeworlds position (fixed forward movement, no backtrack).
- [Confirmed: 5 sources]

---

- **Shortcut (Steps 1-2 skipped):** Rock Cruiser Type C (Tektite) starts with a Crystal crewmember. A previously-unlocked Crystal Cruiser also starts with Crystal crew. Both enter the Hidden Crystal Worlds without the Stasis Pod chain -- but **no quest marker** appears in Rock Homeworlds without Ruwen specifically; you must find the Ancient device by chance.
- **Alternative Crystal Cruiser unlock:** beat the Flagship with Layout A and B of every ship except the Lanius Cruiser (cumulative across all runs).
- **PoNR (whole chain):** if Rock Homeworlds appears before Steps 1-2 are complete the run cannot finish the chain. Per FTL Fandom Wiki: *"as the 2nd step cannot happen at Rock Homeworlds, and the 3rd step HAS TO take place there, and Rock Homeworlds can occur only once per game, therefore unlocking the Crystal Cruiser CANNOT be successful if started from this sector."* Ruwen dying en route also fails the chain permanently.

_source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com Crystal Cruiser + Steam guides) + P2 deep-research cascade 2026-06-02 (ftl.fandom.com Ancestry, Ancient device, Zoltan research facility pages; exact event choices, occurrence %) · capture: web_fetch · confidence: high · enemy-tier: 2 · puzzle-tier: 1 · category: easter-egg · spoiler: late-game_
[Confirmed: 5 sources]

## Achievements
- **Ancestry** (hidden) -- find the Hidden Crystal Worlds with the Rock Cruiser. See `achievements.md`.

## Missability
Entire recruitment path is missable per the chain above; the Hidden Crystal Worlds itself fails permanently if Rock Homeworlds doesn't appear by end of sector 7. See `sections/missables.md`.

## See also
- `items/weapons.md` (Crystal weapons); `items/builds.md` (Crystal Cruiser); `sections/sector_types.md` (Hidden Crystal Worlds, Rock Homeworlds); `factions/crystal.md`.
