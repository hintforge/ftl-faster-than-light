# FTL: Faster Than Light -- Sector Type Notes

**status:** research-integrated
**last_reconciled:** 2026-06-02 (P2 beacon distribution + hazard data added)

FTL is procedural -- there is no fixed sector sequence -- but **sector types** appear in known positional windows and carry consistent event pools. This file holds per-sector-type event/behavior notes. The canonical sector-type list, positional windows, and zone-graph mechanics live in `architecture_manifest.md` and `mechanics.md`; per-sector navigation traversal patterns and the Blue Options table are a P2 target.

> Sector-color note: 48% green / 32% red / 20% purple. **Color is misleading** -- Zoltan (green) sectors are among the most dangerous.

Enemy-ship-behavior and event facts below are `spoiler: progression` (enemy-tier 1) -- written in full, gated from preemptive display at enemy tier 0, available on request. Build tips are `spoiler: none`. Crystal/Last-Stand content is `spoiler: late-game`.

_source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com Sectors + event pages; JP/RU community sources) · capture: web_fetch · confidence: medium · category: mainline_ — governs all entries below; per-entry spoiler tier noted inline.

## civilian_starting / civilian
Sector 1 always (starting); civilian recurs 2-7. Green, easiest.
- `spoiler: none` -- Best place to grind shield/evasion skill at asteroid fields against weak single-laser enemies. [Confirmed: 2 sources incl. JP]
- `spoiler: none` -- The starting sector has fewer stores/quests/nebulas than recurring Civilian sectors despite the shared name. [Single source -- community-wiki]
- `spoiler: progression` (enemy-tier 1) -- Civilian sectors still contain 6-8 hostile encounters; "civilian" ≠ safe. [Confirmed]
- `spoiler: none` -- Guides miss: leftover beacons fall back to the NEUTRAL event list, so "empty" beacons can still fire events. [Single source -- community-wiki]
- `spoiler: none` (P2 beacon distribution) -- Approx. 2-3 stores, 6-8 hostile, 1-2 distress, 2-4 neutral, 0-2 quests, 0-8 nebula. One of the best store-count sectors. [Confirmed: wiki datamining]

## engi_controlled / engi_homeworlds
Recurs / once at 3+. Green, very safe.
- `spoiler: progression` -- Engi **Homeworlds** holds the unique **Engi fleet discussion** event which (with an Engi crewmember) unlocks the **Stealth Cruiser** -- Homeworlds, not the controlled sector. See `factions/engi.md`. [Confirmed: 4 sources]
> **Cross-system dependency** -- see `../dependencies.md` SEQ-001: Engi crew + Engi Homeworlds (not Engi Controlled sector) required to trigger the Stealth Cruiser unlock.
- `spoiler: progression` (enemy-tier 1) -- Hostile Engi events exist (poorly-equipped Engi ships that attack on seeing Federation markings; Engi-virus events spawn Defense Drone II ships) -- the exception to "Engi are always neutral." [Confirmed: 3 sources incl. JP]
- `spoiler: progression` · **missable: yes** -- Engi sectors can host the Damaged Stasis Pod distress event and the Zoltan research facility (Crystal chain steps 1-2). Latest safe before reaching Rock Homeworlds. See `sections/missables.md`, `crew/crystal.md`.
- `spoiler: none` (build) -- Low fight count = less scrap; bring Long-Range Scanners to skip empties.
- `spoiler: none` (P2 beacon distribution) -- Approx. 2-3 stores, 5-7 hostile, 1-3 distress (can exceed 3 due to event-list overflow), 1 quest, 4-6 neutral, 5 item-type. Among the better store-count sectors. [Confirmed: wiki datamining]

## zoltan_controlled / zoltan_homeworlds
Recurs / once at 3+. Green but very dangerous.
- `spoiler: progression` (enemy-tier 1) -- Enemy Zoltan ships have Zoltan Super Shields (5 HP, impenetrable by everything incl. boarding/missiles/bombs until depleted). See `factions/zoltan.md`. [Confirmed: 3 sources]
- `spoiler: progression` · **missable: yes** -- Hosts the **Zoltan research facility** (Crystal chain step 2; yields Ruwen if you carry the Damaged Stasis Pod). Zoltan Homeworlds can be required for some Crystal routing. See `crew/crystal.md`.
- `spoiler: none` (build) -- Bring shield-piercers (missiles/bombs/ion) or boarding to beat Zoltan shields.
- `spoiler: none` (P2 beacon distribution) -- Approx. 2 stores, 6-8 hostile, 1-2 boarders, 2-6 nebula. Deceptive "green" color -- this sector is among the most combat-dense. [Confirmed: wiki datamining]

## mantis_controlled / mantis_homeworlds
Recurs / once at 3+. Red, frequent boarding.
- `spoiler: progression` -- Mantis **Homeworlds** hosts **Legendary thief KazaaakplethKilik**; with a Mantis crew + Lv2 Medbay, crew-kill then spare/heal him to unlock the **Mantis Cruiser**. See `factions/mantis.md`. [Confirmed: 3 sources]
- `spoiler: progression` (enemy-tier 1) -- Mantis ships often carry an Engi (slave) crew; enemy AI may teleport the Engi onto your ship and leave Mantis on repair. [Confirmed: 2 sources]
- `spoiler: none` (build) -- Door upgrades + Mantis/Rock defenders; venting rooms defeats boarders; weak for fragile crews (Zoltan).
- `spoiler: none` (P2 beacon distribution) -- Approx. 1-2 stores, 6-7 hostile, 2-3 empty. Lowest store count of major sectors; scrap-thin. [Confirmed: wiki datamining]

## rock_controlled / rock_homeworlds
Recurs / once at 5+. Red.
- `spoiler: late-game` -- Rock **Homeworlds** holds the **Ancient device** (Crystal chain step 3): with Ruwen alive, a blue option teleports you to the Hidden Crystal Worlds. Once per game, sector 5+ only -- the hard bottleneck of the Crystal unlock. See `crew/crystal.md`. [Confirmed: 5 sources]
- `spoiler: progression` (enemy-tier 1) -- Rock ships have Rock Plating (15% chance to ignore hull damage). Crystal Lockdown Bombs purchasable (rarity 4 controlled / 2 homeworlds). [Confirmed]
- `spoiler: none` (build) -- Fire weapons are weak vs fire-immune Rock crew; bring direct damage.
- `spoiler: none` (P2 beacon distribution) -- Approx. 2 stores, 6-8 hostile, 7-8 neutral. High neutral count means more no-fight / talk/trade events. [Confirmed: wiki datamining]

## pirate_controlled
Recurs 2-7. Red/mixed. (Pirates are not a roster faction -- see `factions/index.md`.)
- `spoiler: progression` -- Can spawn the Damaged Stasis Pod event (Crystal step 1, alongside Engi/Rock sectors); slaver events grant crew of various races. [Confirmed]
- `spoiler: progression` (enemy-tier 1) -- Pirate ships use any race's hulls/crew; disguised distress lures are common.
- `spoiler: none` (P2 beacon distribution) -- Approx. 1-2 stores, 6-8 hostile, 0-5 nebula. Lower store count but high scrap density. [Confirmed: wiki datamining]

## rebel_controlled / rebel_stronghold
Recurs / once at 5+. Red, good scrap. Distinct from the Rebel **Pursuit Fleet** (see `mechanics.md`).
- `spoiler: progression` -- Rebel **Stronghold** hosts the **Rebel shipyard** event: a Flagship prototype under construction; destroy or crew-kill it to unlock the **Federation Cruiser**, delay the fleet 2 turns, and gain a free weapon. See `factions/rebels.md`. [Confirmed: 3 sources]
- `spoiler: none` (build) -- High fight density = high scrap; hunt the shipyard with Long-Range Scanners.
- `spoiler: progression` (P2 fleet mechanic) -- Rebel Controlled sectors add +1 jump to the Rebel Fleet advance on sector entry (a Rebel guard at the entrance beacon). [Confirmed: datamining + community]
> **Cross-system dependency** -- see `../dependencies.md` DEP-009: Entering a Rebel Controlled sector adds +1 jump to the fleet advance counter on entry, shortening the safe-beacon budget by one jump from that point.
- `spoiler: none` (P2 beacon distribution) -- Approx. 1-2 stores, 6-8 hostile, 0-5 nebula. High hostile density = high scrap. [Confirmed: wiki datamining]

## slug_controlled_nebula / slug_home_nebula
Both 4+; home once/game. Purple nebula.
- `spoiler: none` (controls) -- Nebula disables Sensors entirely: no enemy-interior/crew vision unless you have a Slug crew, Lifeform Scanner, or hacking/bomb vision. JP guides advise judging breaches by O2 drop and the breach "boom"/fire crackle sounds. [Confirmed: 3 sources incl. JP]
> **Cross-system dependency** -- see `../dependencies.md` DEP-001: Slug crew counters the nebula Sensor blackout; without one (or Lifeform Scanner), the player has zero interior vision in nebula combat.
- `spoiler: progression` (enemy-tier 1) -- Slug Home Nebula has a unique surrender event; Slug ships sabotage O2; ion storms common. See `factions/slug.md`. [Confirmed]
- `spoiler: none` -- Nebula beacons never have ASB (except when out of fuel). [Confirmed]
- `spoiler: none` (build) -- One Slug crew restores full enemy vision; very strong here. Avoid without it.
- `spoiler: none` (P2 fleet note) -- Nebula beacons within nebula sectors reduce Rebel Fleet advance to only 20% of the normal rate (vs 50% from nebula beacons in non-nebula sectors). Best fleet-delay tool in nebula sectors. [Confirmed: datamining]

## uncharted_nebula
Recurs 2-7. Purple.
- `spoiler: none` (controls) -- Sensors disabled; ~0.8% of these sectors generate with no store (map-gen bug). Slows the Rebel fleet (good for exploration). [Confirmed: 2 sources]
- `spoiler: none` (P2 beacon distribution) -- Approx. 1-2 stores (with the ~0.8% zero-store bug possible); typical nebula mix with sensor blackout. [Confirmed: wiki datamining]

## abandoned_sector
Recurs 2-7 (early best). **AE-only.** Lanius-themed.
- `spoiler: progression` (enemy-tier 1) -- Lanius Scouts (sectors 2-3) are weak and **always have exactly 2 crew**; Lanius Bombers (sector 4+) can carry Teleporter/Mind Control/Cloaking and are among the scariest ships. Lanius kills give better-than-average loot (drone schematics more likely than weapons; higher high-scrap chance). See `factions/lanius.md`. [Confirmed: 3 sources -- guides miss the 2-crew Scout detail]
- `spoiler: none` -- Lanius crew recruitable here (rarity 2); they drain O2 from their room. See `crew/lanius.md`.
- `spoiler: none` (build) -- Take early (S2-3) for easy loot; avoid S6-7 Bombers if under-built.
- `spoiler: none` (P2 beacon distribution) -- Approx. 2 stores; Lanius-themed event pool. [Confirmed: wiki datamining]

## hidden_crystal_worlds
Off-map, reached only after Rock Homeworlds via the Ancient device. Base-game secret.
- `spoiler: late-game` -- Only Crystal weapons/Lockdown Bombs sold; only Crystal crew as rewards. Enemy strength scales to the Rock Homeworlds sector number. Rebels still pursue. Exit teleports to a random post-Rock-HW sector (no choice). See `crew/crystal.md`. [Confirmed: 3 sources]
- `spoiler: late-game` · **missable: yes** -- Requires the full Crystal chain; fails permanently if Rock Homeworlds doesn't appear by end of sector 7, or if Ruwen dies en route.

## the_last_stand
Sector 8 always. Hardest. Hosts the Rebel Flagship (final boss).
- `spoiler: late-game` -- Entry grants 10 hull repair + 10 fuel. Three reusable repair beacons (15 hull + 22-44 scrap, 5 fuel, 4 missiles, 5 drone parts first visit; reusable via Wait). Flagship jumps toward the Base every 2 player jumps; 3 consecutive jumps on the Base = loss. See `mechanics.md` → The Rebel Flagship. [Confirmed: 4 sources]
- `spoiler: late-game` (controls) -- Waiting ticks the map forward and starts the next fight with full FTL charge. Flagship caps your Sensors at level 2.

## Sources
- ftl.fandom.com Sectors and event pages (community-wiki, captured 2026-06-02); Japanese (iphoneac.com, seesaawiki.jp, hatelabo.jp) and Russian (StopGame.ru, ru.fandom.com) community sources; Steam guides.
