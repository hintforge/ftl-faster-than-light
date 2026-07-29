# FTL: Faster Than Light -- Mechanics

**status:** research-integrated
**last_reconciled:** 2026-06-02

Cross-system dependency density: HIGH. FTL's systems interact deeply -- power allocation competes across all systems; weapon types interact (ion drains shields enabling other weapons); crew skill affects system efficiency; fire/breach propagate through rooms; boarding vs. weapon strategies compete for the same power budget.

All numeric values below are **vanilla Advanced Edition** (the default PC/Steam state). Mod wikis (Multiverse, Captain's Edition) were used only to locate vanilla cross-references and are not authoritative for base-game values.

## Power management

The reactor supplies power bars that allocate across systems; powering one system competes with every other.

- **Absolute maximum power = 37** (25 reactor + 8 Zoltan crew + 4 Backup Battery). Reactor caps at 25 bars; reactor upgrade costs run 30 / 20 / 25 / 30 / 35 scrap per 5-bar band.
- Zoltan crew each add +1 free power to their occupied system's room (ion-proof). Backup Battery (AE) supplies +2 / +4 temporary power for 30s on a 20s cooldown and is itself ion-immune.
- _source: P1 deep-research cascade 2026-06-02 (datamining + ftl.fandom.com) · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
- [Confirmed: subagent + community-wiki]

## Shield system

- Each shield bubble = **2 power**, blocks one incoming shot. Shields reach 4 bubbles at level 8.
- Weapon interactions: **lasers / flak / crystal** strip one bubble per shot; **beams** take −1 damage per remaining bubble; **missiles / bombs** ignore bubbles entirely (except a Zoltan Super Shield, which only bombs-with-bypass can pass).
- Recharge ≈ 2s/bubble base. Shields-crew skill (×1.3) and Shield Charge Booster augment (×1.45) multiply **separately**; maximum combined bonus = 1/(1.3×1.45) = 0.531× time (first/second bubble recharge in just over 1s).
- **Zoltan Super Shield:** a 5-HP layer (from enemy Zoltan ships or the Zoltan Shield augment) that is impenetrable by everything -- including boarding, missiles, and bombs -- until depleted.
> **Cross-system dependency** -- see `dependencies.md` DEP-002: Zoltan crew in the Shield room provides +1 ion-proof power bar; two Zoltan guarantee one un-ionizable bubble.
> **Cross-system dependency** -- see `dependencies.md` DEP-008: The Zoltan Shield Bypass augment is the only way to use Teleporter or Mind Control through an enemy Zoltan Super Shield.
- _source: P1 deep-research cascade 2026-06-02 (datamining + ftl.fandom.com) · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
- [Confirmed: subagent + wiki]

## Weapon mechanics

See `items/weapons.md` for the full per-weapon stat tables. Mechanism notes:

- Volley timing is decisive: badly-timed shots get absorbed by regenerating shields. **Beams must fire LAST**, after lasers/flak have dropped the shields.
- Weapon screen position matters -- weapons mounted farther left have longer projectile travel. **Ion Blast travels at half a laser's speed**, so fire it first or stagger volleys.
- Fire proc is rolled **before** breach; a single shot cannot do both.
- Weapon application order: laser/flak/crystal strip shields first (1 bubble/shot); once shields are down the hit room takes hull + system + crew damage. **Crew damage = system damage ×15 HP per occupant.**
- **Charge weapons** keep accumulated charges if Weapons is hacked, unlike normal weapons. The Weapon Pre-Igniter only gives charge weapons one charge / skips one chain cycle -- it does NOT fully charge the Chain Vulcan or Glaive Beam.
> **Cross-system dependency** -- see `dependencies.md` DEP-006: Weapon Pre-Igniter gives charge weapons only one charge after a jump, not a full charge; the Chain Vulcan and Glaive Beam are not fully ready on the first shot.
- **Two ion weapons are dramatically stronger than one** -- the second ion lands before the 5s ion timer expires, enabling infinite shield lockdown. (Under-emphasized on the English wiki; surfaced by Japanese sources iphoneac.com / hatelabo.jp.)
- The **Anti-Bio Beam** must physically cross the tile a crew member stands on (unlike other weapons, which damage everyone in a hit room).
- _source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com + JP iphoneac.com/hatelabo.jp + subagent) · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
- [Confirmed: 2+ sources incl. Japanese -- ion-stacking insight extends English wiki]

## Engine system & evasion

- **+5% evasion per Engines bar** (requires an operational Piloting subsystem with a crew member in the room).
- Engines manning skill adds +5 / +7 / +10% by skill level; Piloting manning adds up to +20% "free." Autopilot (no Piloting crew) yields 50% (Piloting-2) / 80% (Piloting-3) of engine evasion. **Hacked or unmanned Piloting/Engines = 0% evasion.**
- Practical evasion wall ≈ 45%; active Cloak adds a flat +60% (unaffected by anything, fills toward 100%). **Beams can never be dodged.**
- _source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com + datamining) · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
- [Confirmed: 4 sources]

## FTL drive & sector progression

- 8-sector run structure; sector 1 is always the Civilian (Starting) Sector and sector 8 is always The Last Stand.
- **Rebel Fleet pursuit:** the fleet advances as a red shaded area from the left; datamined, the pursuit value increases by 0x40 per jump (≈ one beacon "column" per jump). Visiting a nebula beacon **in a non-nebula sector halves** the advance that turn; visiting a nebula beacon **while inside a nebula sector** reduces it only partially (by 1/5 of the regular rate). Letting a Rebel scout/auto-ship escape (or not jumping before it does) **doubles** pursuit for 1 turn. Hiring a mercenary delays the fleet 2 turns; the Distraction Buoys augment postpones advancement by 1 turn at sector start.
- **Exit beacon:** always present and visible, on the opposite side from start; reaching it opens the next-sector choice (edge type: story-gate). Within a sector you may revisit beacons (1 fuel each); between sectors there is **no backtracking** after jumping (one-way edge).
- _source: P1 deep-research cascade 2026-06-02 (Rebel Fleet wiki page + FearLess Cheat Engine datamining) · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
- [Confirmed: 4 sources incl. datamining]

> Sector-type event pools and per-sector navigation notes live in `sections/sector_types.md`. The Rebel **Pursuit Fleet** (above) is distinct from **Rebel Controlled Sectors** (mid-late hostile sectors) -- see `factions/rebels.md`.

## Oxygen, fire, and breach

- **Oxygen:** the O2 system refills ship air (levels 1-3). When O2 is offline or a room is breached/vented, air drops; crew suffocate in vacuum (species modifiers apply -- Crystal take 0.5× suffocation damage; Lanius are immune and actively drain O2 from their room).
> **Cross-system dependency** -- see `dependencies.md` DEP-010: Lanius crew drain O2 from their room; non-immune crewmates sharing that room suffocate faster when the O2 system is under strain.
> **Cross-system dependency** -- see `dependencies.md` DEP-004: Rock crew are fully fire-immune and can stand in burning rooms to fight or repair.
- **Fire:** ignites via weapon proc chance (and Fire Beam/Fire Bomb at high %); spreads to adjacent rooms per tick; damages systems and crew. Extinguished by crew repair-speed, by venting the room to vacuum, or by O2 depletion. **Rock crew are fire-immune**; Fire Suppression augment auto-extinguishes all fires.
- **Breach:** created by some weapons (% per shot), asteroids, and guaranteed by Boarding Drones. Causes O2 loss (no extra hull damage) and must be sealed before the room can be manned/repaired. **Seal speed = repair speed** (12.5s/bar for an untrained human).
- _source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com + JP sources) · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
- [Confirmed]

## Crew combat & boarding

- Melee damage scales by species modifier (Mantis 2×, Engi/Zoltan 0.5×). Room number-advantage matters; the AI flees suffocating rooms -- **vent everything but the Medbay** so boarders cluster where you can heal-tank.
- **Teleporter** bypasses shields entirely on beam-up, but **cannot teleport onto a cloaked ship or through a Zoltan Super Shield** (unless you carry Zoltan Shield Bypass). Teleporter L2 recharges before suffocation; L3 allows spamming. Crew left aboard the enemy at FTL jump are **lost permanently, even with a Clone Bay**.
> **Cross-system dependency** -- see `dependencies.md` DEP-005: Neither Teleporter nor Boarding Drone can act on a cloaked ship; Cloaking provides full boarding immunity while active.
- **Clone Bay (AE)** revives dead crew on jump (or on Wait, per a dev patch) with skill loss; it **cannot heal mid-fight** (the key difference from Medbay), is **incompatible with Medbay**, and Engi Med-bot Dispersal does not work with it. Clone Bay + boarding = low-risk aggression (dead boarders re-clone on jump).
> **Cross-system dependency** -- see `dependencies.md` DEP-003: Clone Bay and Medbay are mutually exclusive; installing one prevents the other; Engi Med-bot Dispersal healing also stops working with Clone Bay.
- _source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com + JP sources + dev quote Matthew Davis) · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
- [Confirmed: 2 sources + dev quote]

## Cloaking

- Active cloak grants a flat **+60% evasion** and **stops enemy weapon charge** for its duration. Your own weapons keep charging during cloak (use the Stealth Weapons augment to fire without decloaking). Cloak as the enemy volley is mid-flight to dodge it.
> **Cross-system dependency** -- see `dependencies.md` DEP-011: Stealth Weapons augment is required to fire during Cloaking without cancelling the cloak effect.
- _source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com) · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
- [Confirmed]

## Hacking (Advanced Edition)

- Disables one targeted enemy system for **4 / 7 / 10s** (L1/2/3). The hacking pulse must finish before the cooldown; it **cannot launch through a Zoltan Super Shield** even with bypass. Hacked doors become level-3 blast doors that self-heal in 7s. Hacked Piloting/Engines drops enemy evasion to 0. Hacking Drone Control has a 39 / 62 / 77% chance (L1/2/3) to destroy a drone.
- _source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com + subagent) · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
- [Confirmed: subagent + wiki]

## Mind Control (Advanced Edition)

- Controls one enemy crew member for **14 / 20 / 28s** (L1/2/3); L2-3 boost the controlled crew's HP and combat. Blocked by a Zoltan Super Shield (unless bypass). **Slugs and Lanius are immune.** Cooldown resets on jump; full ionization caps cooldown at 25s.
- _source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com) · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
- [Confirmed]

## Scrap & economy

- **Scrap** is the universal currency. Reward scales with sector number × difficulty (lower difficulty gives MORE scrap; resource rewards are fixed). Scrap Recovery Arm augment adds +10% from all sources (not selling); Repair Arm adds +2 hull per scrap pickup but −15% scrap. Hull-repair store price scales with sector number.
- Thresholds: **600+ scrap on hand** = "Scrap Hoarder" achievement; **10,000 cumulative across all games** = "Rule Ten: Greed is Eternal."
- _source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com + subagent) · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
- [Confirmed: subagent + wiki]

## Run resources

- **Fuel:** 1 consumed per jump (including backtracking); all ships start with 16. Costs 3/unit at stores, 2 at refueling events. At 0 fuel you may "Wait" (the fleet still advances; enemies start charging FTL and jump after ~90s). Beating an Elite Fighter at an overtaken beacon gives 1 fuel (4 if you were out of fuel).
- **Missiles:** 1 consumed per missile/bomb volley (Swarm/Pegasus use 1 for a multi-shot). Explosive Replicator augment = 50% chance not to consume.
- **Drone Parts:** consumed deploying drones and launching hacking drones; recoverable with the Drone Recovery Arm (external drones only, jump after 2 repairs).
- **Crew:** maximum 8; runs start with 1-4; a 9th forces you to relieve one.
- _source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com + subagent) · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_
- [Confirmed]

## Builds / loadouts

Build recommendations (interpretation, not falsifiable claims -- no claim metadata):

- **Weapon-focused gunship:** Kestrel A or similar; target a guaranteed ~7-damage volley (e.g. Burst Laser II + Flak I, plus a Halberd Beam to finish). Prioritize Shields → Engines → Cloaking. Mainstream community pick; the Burst Laser II is the consensus best all-rounder.
- **Drone-focused:** Engi A; lean on a Combat Drone + Defense Drone I, ion support, and Drone Control. Weaker burst but strong automation; "Technophobia" (no drones) is the opposite constraint.
- **Boarding-focused:** Mantis A or a 2-Mantis teleporter plan; pair with a Clone Bay so dead boarders re-clone on jump. Door upgrades + Mantis/Rock defenders hold off enemy boarders; venting rooms defeats them. Weak for fragile crews (Zoltan).
- **Hybrid / control:** Hacking + a modest weapon set. Hacking shields to guarantee a Flagship missile-launcher kill carries otherwise-weak builds.
- **General progression:** Shields (2 bubbles by sector 3) → Medbay/Clone Bay → Cloaking → Hacking → Teleporter. Keep ~40-45% evasion. Buy a Defense Drone I against missile ships.

## The Rebel Flagship (final boss)

> Gated at **enemy tier 2+** -- no phase details volunteered at tier 0/1. Available on request at any tier (post-encounter help is permitted even at tier 0). The following is `spoiler: late-game`.

- The final boss has **3 phases**, all fought in The Last Stand. It jumps toward the Federation Base every 2 player jumps; **3 consecutive jumps on the Base = loss.** Each phase repairs the Flagship's hull, systems, and fires, but **crew deaths persist** between phases. Killing the entire crew turns it into a self-repairing auto-ship -- so leave the laser-room crewman alive.
> **Cross-system dependency** -- see `dependencies.md` DEP-012: Crew kills via boarding in Phase 1 carry forward; killing all crew makes the Flagship an un-boardable auto-ship in later phases.
- **Phase 1:** four weapon systems -- triple-missile launcher, ion cannon, laser, beam (+ Hacking in AE; cloaks at start). Kill the missiles first (use boarders), then the laser; cloak the missile volley.
- **Phase 2:** loses cloak and the ion weapon; focuses on drones. A "Power Surge" spawns 10+ anti-ship drones (attacking Drone Control does NOT stop the surge). Defense Drone I shoots down its boarding drones.
- **Phase 3:** gains a Zoltan Super Shield (regenerates on Power Surge), Mind Control, and a Teleporter; the Power Surge fires a 7-shot laser barrage or refills the shield. ~28% dodge, 3-4 base shields; missile/laser Artillery jump to Level 4. Cloak the SECOND missile volley to also dodge the surge.
- **Critical target every phase:** knock out the missile launcher (you need a reliable ~7 damage). Hacking + boarding trivialize the fight.
- **Difficulty scaling:** on Easy + AE-off the Flagship has only 3 shield layers (shield L6) instead of 4 (L8). On Hard it gains 2 extra rooms linking the Laser/Missile mounts to the main ship (harder to stop repairs), and having >25% evasion puts your Piloting/Engines on its high-priority target list.
- _source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com + Steam guides) · capture: web_fetch · confidence: medium · enemy-tier: 2 · puzzle-tier: 0 · category: mainline · spoiler: late-game_
- [Confirmed: 4-5 sources] · see `factions/rebels.md` for full summary

## Blue Options (Locks-and-Keys)

_source: P2 deep-research cascade 2026-06-02 (ftl.fandom.com Blue Options master list; JP seesaawiki.jp/ftl + iphoneac.com; RU ftl.fandom.com/ru; Steam Community; Subset Games Forum) · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline_

Blue Options are FTL's lock-and-key event system: ~143 events offer an additional highlighted choice when the player has a specific crew species, augmentation, system, weapon, drone, or story flag aboard. **They are always visible-but-greyed** when you lack the key -- the requirement is shown in parentheses next to the choice; they are never hidden. [Confirmed: 5 sources, 2 languages]

`spoiler: none · enemy-tier: 0 · puzzle-tier: 0`

**Exception rule: blue ≠ always better.** Several blue options carry a "[no benefit]" or "advice role only" tag, or serve only the Diplomatic Immunity achievement. Some merely avoid a fight, which lowers score if you are score-optimizing. Check the outcome before assuming. [Confirmed: wiki + RU Fandom]

### Crew-species keys

`spoiler: none · enemy-tier: 0 · puzzle-tier: 0` — key requirement and general outcome type; existence of the option visible from game start.

| Key (crew) | Representative events | Blue outcome category | Visible? |
|---|---|---|---|
| **Human** | Rebel checkpoint (all-human ships pass) | Avoid fight / free passage | greyed |
| **Engi** | Engi distress call; Malfunctioning defense system; Refugee ship trading; The Engi virus; Two smashed Engi ships; Unknown disease on mining colony | Repair/bypass, free scrap/items | greyed |
| **Zoltan** | Federation terraforming team C12 (≈Sensors 2-3); Zoltan trade hub | Better trade / map info | greyed |
| **Mantis** | Confused Mantis; Slug oxygen malfunction | Recruit/crew outcomes | greyed |
| **Rockman** | Crystalline research facility; Fire on small research station; Mantis ship with Rock body parts; Rock armoured transport; Slug drink; Unknown disease on mining colony | Fire immunity, recruit, safe outcome | greyed |
| **Slug** | Disabled Rock transport; Intelligent lifeform on planet; Nebula ships exchange fire; Poorly armed Slug ship; Single life form on moon; The Black Raven; Zoltan security checkpoint (≈Mind Control) | Nebula vision, recruit | greyed |
| **Lanius** (AE) | Civilians fleeing/under fire from Lanius; Lanius absorbing beacons/rebel base; Lanius salvaging; Lanius scavenger trader; Merchant/science craft docked with Lanius; Space station under construction; The Engi virus | Negotiate, salvage, recruit | greyed |
| **Crystal** | Crystal civilian question; Crystalline cache (≈Breach Missiles) | Scrap/loot | greyed |

`spoiler: progression · enemy-tier: 0 · puzzle-tier: 0` — ship-unlock outcomes (homeworld events, mid-game):

| Key (crew) | Event | Blue outcome |
|---|---|---|
| **Engi** | Engi fleet discussion (Engi Homeworlds) | Stealth Cruiser unlock |
| **Mantis** | Legendary thief KazaaakplethKilik (Mantis Homeworlds) | Mantis Cruiser unlock |
| **Slug** | Slug Home Nebula surrender | Slug Cruiser unlock |

`spoiler: late-game · enemy-tier: 0 · puzzle-tier: 0` — Crystal sector access:

| Key (crew) | Event | Blue outcome |
|---|---|---|
| **Crystal** | Ancient device (Rock Homeworlds) | Crystal sector entry |

### Augmentation keys

`spoiler: none · enemy-tier: 0 · puzzle-tier: 0`

| Key (augment) | Events | Blue outcome | Visible? |
|---|---|---|---|
| **Long-Ranged Scanners** | Destroyed cargo ship; Encrypted federation signal; Engi distress call; Engi research station; Federation ship in need of aid; Heavily damaged Federation ship; Prepare to dock; Rebel ship in nebula; Small asteroid belt distress | Map/intel, safe approach | greyed |
| **Lifeform Scanner** (AE) | Drifting debris; Rebel ship in nebula; Small research station with no response | Detect crew/lifeforms | greyed |
| **Rock Plating** | Dense asteroid field distress; Mantis ship with Rock body parts; Small asteroid belt distress | 100% safe asteroid search (vs 1/3 default) | greyed |
| **Engi Med-bot Dispersal** | Dedicated event category | Heal/cure outcome | greyed |
| **Backup DNA Bank** (AE) | Dedicated event category | Crew-preservation outcome | greyed |
| **Scrap Recovery Arm** | Dedicated event category | Extra scrap | greyed |
| **Distraction Buoys** | Sector start beacon | Delay Rebel fleet 1 turn | greyed |

`spoiler: late-game · enemy-tier: 0 · puzzle-tier: 1` — Crystal chain key:

| Key (augment) | Events | Blue outcome | Visible? |
|---|---|---|---|
| **Damaged Stasis Pod** | Zoltan research facility (Crystal chain step 2) | Revives Crystal crew Ruwen | greyed |

### System keys

`spoiler: none · enemy-tier: 0 · puzzle-tier: 0`

| Key (system) | Events | Blue outcome | Visible? |
|---|---|---|---|
| **Med Bay (lvl 2-3)** | Many distress/crew-rescue events | Save crew + gain scrap/crew | greyed |
| **Clone Bay** (AE) | Abandoned space station; Nebula ships exchange fire; Single life form on moon; Space station under construction | Crew-safe outcomes | greyed |
| **Door System (lvl 2-3)** | Damaged space station; Merchant's request; Nebula ships exchange fire; Single life form on moon; Slug sabotage events; Small research station | Crew safety/reward | greyed |
| **Sensors (lvl 2-3)** | Auto-ship near sensor station; Destroyed cargo ship; Engi research station; Prepare to dock; Rebel ship nearby; Rock deserters; many map-reveal events | Reveal sector map / data | greyed |
| **Piloting (lvl 2-3) / Engines** | Escape events; Auto-ship fight in plasma storm (Engines 6-8); Confused Mantis | Guaranteed escape / engine upgrade reward | greyed |
| **Crew Teleporter** | Auto-ship near sensor station; Federation/heavily-damaged Federation ship; Friendly slaver (lvl 2+); Merchant's request; Small asteroid belt distress; Small research station; Unencrypted comm channel; Zoltan trade hub | Board for loot/crew | greyed |
| **Drone Control** | Pirate ship selling drones; Small asteroid belt distress | Buy/deploy drone outcome | greyed |
| **Hacking** (AE) | Auto-ship near small space-station | Bypass defenses | greyed |
| **Mind Control** (AE) | Black market weapons trader; Confused Mantis (superior to Mantis crew); Large trade station; Merchant's request; Zoltan security checkpoint (≈Slug) | Better/forced outcome | greyed |
| **Cloaking** | Auto-ship fight in plasma storm | Evade/escape | greyed |

`spoiler: progression · enemy-tier: 0 · puzzle-tier: 0` — ship-unlock system keys:

| Key (system) | Event | Blue outcome |
|---|---|---|
| **Clone Bay** or **Door System (lvl 2-3)** | KazaaakplethKilik (Mantis Homeworlds) | Mantis Cruiser unlock path |
| **Crew Teleporter (lvl 2+)** | KazaaakplethKilik; Crystalline cache | Ship unlock / Crystal loot |

### Weapon and drone keys

`spoiler: none · enemy-tier: 0 · puzzle-tier: 0`

| Key | Events | Blue outcome | Visible? |
|---|---|---|---|
| **Artillery Beam** (Fed Cruiser only) | Crushed pirate | Free loot | greyed |
| **Beam weapon** | Crushed pirate | Free loot | greyed |
| **Anti-Bio Beam** (AE) | Giant alien spiders; Unencrypted comm channel | Clear infestation safely | greyed |
| **Fire Bomb / Fire Beam** | Mantis war camp; Remote settlement; Unencrypted comm channel | Burn/clear outcome | greyed |
| **Ion weapon** | Malfunctioning defense system | Disable safely | greyed |
| **Hull-Repair Drone** | Mantis ships battle for Rock freighter | [no benefit] -- Diplomatic Immunity only | greyed |
| **Boarding/Combat/Beam/Defense/Anti-Personnel/System-Repair Drones** | Various auto-ship & distress events | Repair/combat outcomes | greyed |

`spoiler: late-game · enemy-tier: 0 · puzzle-tier: 1` — Crystal chain weapon key:

| Key | Events | Blue outcome | Visible? |
|---|---|---|---|
| **Breach Missiles** (AE) | Crystalline cache (≈Crystal crew as alternative) | Open cache | greyed |

### Achievement- and flag-triggered

`spoiler: progression · enemy-tier: 0 · puzzle-tier: 0`

**Diplomatic Immunity achievement:** No blue options are *gated by* achievements; the relationship is inverse -- the achievement is *earned by using* 4 crew-species blue options before entering Sector 6 (Federation Cruiser only). Per the FTL Fandom Wiki: *"only blue event choices that arise as a result of having particular alien crewmembers aboard count -- system upgrades, augments, or weapons do not."* Cutoff: the *exit beacon of Sector 5* is the last possible opportunity (entering Sector 6 = cutoff). [Confirmed: wiki]
> **Cross-system dependency** -- see `dependencies.md` SEQ-003: Diplomatic Immunity requires 4 alien crew blue events on the Federation Cruiser before the Sector 5 exit beacon; system/augment/weapon blue options do not count.

**Multi-stage flag chains:** Confused Mantis pursuit and Slug Home Nebula surrender quest marker also gate later blue options on having triggered the earlier step in the same run. [Confirmed]

`spoiler: late-game · enemy-tier: 0 · puzzle-tier: 1`

**Crystal chain (principal flag chain):** The Damaged Stasis Pod → Crystal crew Ruwen → Ancient device sequence is the longest flag chain in the game; each step's blue option requires the item/flag set by the previous step. Full chain in `crew/crystal.md` and `sections/missables.md`.

_source: P2 deep-research cascade 2026-06-02 · confidence: medium_
[Confirmed: 5 sources, 2 languages]

## Sources

- ftl.fandom.com (Sectors, Rebel Fleet, Shields, Weapons, Systems, Crystal Cruiser pages, Blue Options master list) -- community-wiki, Cloudflare-gated for automated fetch; deep-research cascade captured 2026-06-02
- Japanese: iphoneac.com (data tables), seesaawiki.jp/ftl, hatelabo.jp (attack-side strategy), game-pcs.com, gorakuhunter.com -- editorial-non-en
- Russian: StopGame.ru, gamin.me, ru.fandom.com FTL wiki -- editorial-non-en
- Datamining: FearLess Cheat Engine (pursuit value 0x40/jump); community proc-rate / timing tables
- Steam Community 100% Achievement Guide (id=3667584738); Steam Blue Events List guide
