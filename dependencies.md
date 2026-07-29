# Dependencies -- FTL: Faster Than Light
<!-- hintforge · stitch pass · last run: 2026-06-03 -->
<!-- Every stitch run re-audits ALL existing edges + adds new ones. The per-edge convergence audit (open each cited source, verify the specific value) applies to every row in this file on every run, not just new candidates. A game patch, DLC, or new ingestion phase can change facts that existing edges cite -- only a full re-audit catches that. See `stitch_and_zipper.md` Phase B "Re-run scope: always full." Inconsistencies (cited source contradicts edge text) land in the `## Corpus inconsistencies` section; the edge row stays in place. -->

## Cross-system edges

| Edge ID | System A | System B | Dependency description | Confidence | Source files |
|---------|----------|----------|------------------------|------------|--------------|
| DEP-001 | Slug crew species | Sensors system / nebula sectors | Slug crew provides enemy-interior vision (crew positions + room states) in nebula sectors where the Sensors system is fully disabled; without a Slug crewmember (or Lifeform Scanner augment as substitute), the player has zero interior vision in nebula combat. | high | crew/slug.md, sections/sector_types.md, factions/slug.md |
| DEP-002 | Zoltan crew species | Shield system | Each Zoltan crewmember in the Shield room adds +1 ion-proof power bar to the Shield system; two Zoltan in the Shield room guarantee at least one shield bubble that cannot be removed by ion weapons. | high | crew/zoltan.md, mechanics.md |
| DEP-003 | Clone Bay system | Medbay system | Clone Bay and Medbay are mutually exclusive ship systems -- a ship cannot have both installed simultaneously. Additionally, the Engi Med-bot Dispersal augment's crew-healing effect is disabled when a Clone Bay replaces the Medbay. | high | items/systems.md, mechanics.md, items/augmentations.md |
| DEP-004 | Rock crew species | Fire propagation mechanic | Rock crew are fully immune to fire damage, enabling them to stand in burning rooms to fight or repair without taking crew damage; fire-based weapons (Fire Beam, Fire Bomb) and fire proc from other weapons deal zero crew damage to Rock crew encountered on enemy ships. | high | crew/rock.md, mechanics.md, sections/sector_types.md |
| DEP-005 | Teleporter system / Boarding Drone | Cloaking system | Neither the Crew Teleporter nor a Boarding Drone can target or land on a cloaked ship; active Cloaking provides full immunity to boarding attempts for its duration, regardless of the attacker's system level. | high | items/drones.md, mechanics.md |
| DEP-006 | Weapon Pre-Igniter augment | Charge weapons (Chain Vulcan, Glaive Beam, Laser Charger, Ion Charger, Swarm Missile) | The Weapon Pre-Igniter gives charge weapons only ONE charge after a jump (skips one charge cycle), not a full charge; it does not fully charge the Chain Vulcan or Glaive Beam before the first shot. The augment fully charges non-charge weapons normally. | high | items/augmentations.md, mechanics.md |
| DEP-007 | Crystal Vengeance augment | Sweet Revenge achievement (#46) | The Crystal Vengeance augment is the sole trigger for achievement #46 Sweet Revenge; the achievement requires killing an enemy with the shard fired by Crystal Vengeance's 10%-proc counter-shot. Without this augment the achievement cannot be earned. | high | items/augmentations.md, achievements.md, crew/crystal.md |
| DEP-008 | Zoltan Shield Bypass augment | Teleporter system / Mind Control system | The Zoltan Shield Bypass augment is the only way to use the Crew Teleporter or Mind Control through an enemy Zoltan Super Shield; without it, both systems are fully blocked by the Super Shield even after all normal shields are stripped. | high | items/augmentations.md, mechanics.md |
| DEP-009 | Rebel Controlled sector type | Rebel Fleet advance counter | Entering a Rebel Controlled sector adds +1 jump to the Rebel Fleet advance counter at the sector entrance beacon (a Rebel guard fight at the entrance); this is in addition to the standard +0x40-per-jump advance, effectively shortening the safe-beacon budget by one jump from the moment of entry. | high | sections/sector_types.md, architecture_manifest.md |
| DEP-010 | Lanius crew species | O2 system / room oxygen | Lanius crew actively drain O2 from whichever room they occupy; if the O2 system is under strain (damaged, vented, or absent) or a Lanius is placed in a room with non-immune crewmates, those crewmates will suffocate faster than normal O2 loss would cause. | high | crew/lanius.md, mechanics.md, sections/sector_types.md |
| DEP-011 | Stealth Weapons augment | Cloaking system | The Stealth Weapons augment allows weapons to fire during active Cloaking without cancelling the cloak; without it, firing any weapon immediately ends the cloak, sacrificing the evasion window and stopping enemy-weapon-charge suppression prematurely. | high | items/augmentations.md, mechanics.md |
| DEP-012 | Boarding / crew-kill strategy (Rebel Flagship Phase 1) | Rebel Flagship Phases 2-3 behavior | Crew killed via boarding in Rebel Flagship Phase 1 remain permanently dead in Phases 2 and 3 (crew deaths persist across phases); killing ALL Flagship crew converts the ship into a self-repairing auto-ship that cannot be boarded and regenerates systems -- at least one crew member (conventionally the laser-room crew) should be left alive to prevent this. | high | mechanics.md, factions/rebels.md |

## PoNR / lockout edges

| Edge ID | Trigger | Locked out | Notes | Source files |
|---------|---------|------------|-------|--------------|

_No stitch-discovered PoNR edges this pass. Crystal chain PoNRs are documented as entity facts in `crew/crystal.md` and `sections/missables.md`._

## Missable / sequencing dependencies

| Edge ID | Action | Window | Consequence | Source files |
|---------|--------|--------|-------------|--------------|
| SEQ-001 | Have an Engi crewmember aboard when the Engi fleet discussion event spawns | Engi Homeworlds only (sector 3+, once/game); NOT available in regular Engi Controlled sectors | Without an Engi crew, the blue option for the Engi fleet discussion does not trigger and the Stealth Cruiser cannot be unlocked via this event in the run | factions/engi.md, items/builds.md, sections/sector_types.md, mechanics.md |
| SEQ-002 | Crystal chain Steps 1 and 2 can both appear in Engi sectors (different event triggers: Step 1 at distress beacons, Step 2 at normal beacons) | Before reaching Rock Homeworlds (which locks Step 2 out permanently) | A player can complete both Crystal chain prerequisites without leaving Engi space; finding Step 2 in an Engi sector does not require Step 1 to have occurred elsewhere | crew/crystal.md, sections/missables.md |
| SEQ-003 | Use 4 crew-species blue events on the Federation Cruiser | Before passing the exit beacon of Sector 5 (the hard cutoff) | Only alien crewmember keys count toward Diplomatic Immunity (#35); system, augment, and weapon blue options do NOT count; missing the S5 exit beacon cutoff makes the achievement unearnable that run | achievements.md, mechanics.md, items/builds.md |

## Stitch run log

| Date | Scope | Edges written | Edges proposed (pending) | Inconsistencies surfaced | Model |
|------|-------|---------------|--------------------------|--------------------------|-------|
| 2026-06-03 | full | 15 (12 DEP + 0 PON + 3 SEQ) | 0 | 1 | sonnet-class |

## Corpus inconsistencies

Stitch's per-edge convergence audit (see [`../../hintforge/stitch_and_zipper.md`](../../hintforge/stitch_and_zipper.md) Phase B) populates this section when a candidate edge's cited sources contradict each other.

| Detected | Files | Conflicting values | Suspected authoritative source | Status |
|----------|-------|--------------------|--------------------------------|--------|
| 2026-06-03 | crew/mantis.md, factions/mantis.md, items/builds.md, sections/sector_types.md vs mechanics.md | Four files state the Mantis Cruiser unlock (KazaaakplethKilik) requires "Mantis crew + Lv2 Medbay"; mechanics.md Blue Options system-keys table lists "Clone Bay or Door System (lvl 2-3)" as the system blue-option key for this event with no Medbay entry. These may be partially compatible (Medbay is one route; Clone Bay/Door System are alternatives) or the four-file description may be oversimplified. | mechanics.md Blue Options (P2 ingestion from wiki datamining) -- but the four-file consensus is strong; user or P3 re-research recommended to confirm actual blue-option trigger vs recommended-loadout distinction | open |
