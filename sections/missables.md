# Sections -- Missables

**status:** research-integrated
**last_reconciled:** 2026-06-02 (P2 exact event detail added)

Aggregated catalog of missable content -- "what am I about to lose if I leave this section?" -- built from every `missable: yes` overlay claim in the corpus. Per-run opportunities are noted; FTL is a roguelike, so most "misses" cost the current run, not permanent progress, **except** the Crystal Cruiser unlock (a permanent unlock that can be lost for the run if the chain breaks).

_source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com Crystal Cruiser + event pages; Steam guides) · capture: web_fetch · confidence: high · category: easter-egg_

## The Crystal Cruiser unlock chain (missable -- the big one)

> `spoiler: late-game` · enemy-tier 2 · puzzle-tier 1. Required for the **Ancestry** achievement. Full step detail in `crew/crystal.md`. Each step is `missable: yes`.

| Step | Event | Where | Latest-safe / PoNR | P2 detail |
|---|---|---|---|---|
| 1 | Damaged Stasis Pod (distress beacon, "Dense asteroid field") | `pirate_controlled`, `engi_controlled`, `engi_homeworlds`, `rock_controlled`, or `rock_homeworlds` | Before reaching Rock Homeworlds | Rock Plating = 100% success; without it ~1/3 chance. Occurrence: ~60% Engi, ~69% Pirate, ~75% Rock |
| 2 | Zoltan research facility (revives Ruwen) | `engi_controlled`, `engi_homeworlds`, `zoltan_controlled`, or `zoltan_homeworlds`; **cannot occur in Rock Homeworlds** | Before Rock Homeworlds | Blue option requires Damaged Stasis Pod; Engi sectors can host both Step 1 and Step 2 |

> **Cross-system dependency** -- see `../dependencies.md` SEQ-002: Engi sectors can host both Steps 1 and 2 using different event triggers (Step 1 at distress beacons, Step 2 at normal beacons); both prerequisites can be completed without leaving Engi space.
| 3 | Ancient device (teleport to Crystal Worlds) | **Rock Homeworlds** (sector 5+, once/game); quest beacon appears if Ruwen alive | Must reach Rock HW by sector 7 | Any Crystal crew triggers the blue option; only Ruwen creates the quest beacon |
| 4 | 2nd quest marker in Hidden Crystal Worlds → Crystal Cruiser unlock | Hidden Crystal Worlds (off-map) | Within the Crystal Worlds visit | Rewards: Crystal Cruiser unlock, Crystal Vengeance augment, fuel/scrap/hull repairs |

- **PoNR for the whole chain:** if Rock Homeworlds appears before Steps 1-2 are complete, the run cannot finish the chain. Per FTL Fandom Wiki: *"the 2nd step cannot happen at Rock Homeworlds, and the 3rd step HAS TO take place there."* Ruwen dying en route also fails it permanently.
- **Shortcut:** Rock Cruiser Type C (Tektite) or a previously-unlocked Crystal Cruiser starts with Crystal crew (skips Steps 1-2; still need to find Ancient device, with no quest marker unless Ruwen specifically).
- [Confirmed: 5 sources; P2 occurrence % from wiki datamining]

## Per-run ship-unlock opportunities (not flagged missable in P1, but run-bound)

These unlocks are permanent once earned, but each requires a specific sector type / event to appear in the run:
- **Stealth Cruiser** -- Engi fleet discussion (Engi Homeworlds, needs Engi crew).
- **Mantis Cruiser** -- spare KazaaakplethKilik (Mantis Homeworlds, needs Mantis crew + Lv2 Medbay).
- **Federation Cruiser** -- Rebel shipyard (Rebel Stronghold) or beat Flagship w/ Engi.
- **Zoltan Cruiser** -- Zoltan peace event.

See `items/builds.md` and the relevant `factions/` files.

## Sources
- ftl.fandom.com Crystal Cruiser and event pages (community-wiki, captured 2026-06-02); Steam Community guides.
