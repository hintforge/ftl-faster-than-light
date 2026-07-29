# FTL: Faster Than Light -- Factions

**status:** research-integrated
**last_reconciled:** 2026-06-02
**class:** factions

## Why this file exists

The corpus's roster for FTL's factions/alien races -- the groups the player meets as enemies, traders, or event participants, each with distinct ship designs, event pools, and behavioral tendencies. Unlike the playable crew species in `crew/`, these are faction-level entities. FTL has **no formal reputation system**; faction encounters are event-driven.

## Roster (9 factions)

| entity-id | display name | entity-status | per-faction file | notes |
|---|---|---|---|---|
| federation | Galactic Federation | friendly | `factions/federation.md` | Player's faction; Artillery-defined cruiser |
| rebels | The Rebellion | hostile | `factions/rebels.md` | Pursuit fleet + Rebel Flagship final boss |
| engi | Engi | neutral | `factions/engi.md` | Mostly neutral; documented hostile exceptions |
| mantis | Mantis | hostile | `factions/mantis.md` | Aggressive; boarding crews; carry Engi slaves |
| rock | Rock | neutral | `factions/rock.md` | Rock Plating ships; Ancient device (Crystal chain) |
| slug | Slug | hostile | `factions/slug.md` | Nebula dwellers; sabotage O2 |
| zoltan | Zoltan | neutral | `factions/zoltan.md` | Super-Shield ships; research facility (Crystal chain) |
| crystal | Crystal | neutral | `factions/crystal.md` | Hidden Crystal Worlds; gated |
| lanius | Lanius | hostile | `factions/lanius.md` | AE only; Scouts (2 crew) / Bombers |

> Note: **Pirates** are not a roster faction -- Pirate Controlled is a sector type whose ships use any race's hulls/crew (disguised distress lures are common). See `sections/sector_types.md`.

## The Rebel Flagship
The game's final boss (3 phases) is the Rebellion's primary military threat. Gated at enemy tier 2+. Full breakdown in `mechanics.md` → "The Rebel Flagship (final boss)"; summary in `factions/rebels.md`.

## Sources
- See per-faction files for source lists (P1 deep-research cascade, 2026-06-02). Primary: ftl.fandom.com faction/ship pages; Japanese and Russian community sources.
