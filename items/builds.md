# FTL: Faster Than Light -- Ships & Builds

**status:** research-integrated
**last_reconciled:** 2026-06-02

Ship roster, layout/unlock conditions, and starting loadouts. Build-archetype strategy (weapon / drone / boarding / hybrid) lives in `mechanics.md` ("Builds / loadouts").

## Ship roster (10 classes × 3 layouts → 28 playable)

There are 10 ship classes. Most have layouts A, B, and C; **Crystal and Lanius have only A and B** (no Type-C), giving 28 playable configurations.

- **Layout A:** complete the ship's quest event OR beat the Flagship with the previous ship in the chain.
- **Layout B:** earn 2 of the 3 ship-specific achievements.
- **Layout C:** reach sector 8 with Layout B and AE enabled (no C for Crystal/Lanius).

_source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com ship pages + Steam guides + subagent) · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression_ — unlock events are mid-game-gated. [Confirmed: 5 sources]

| Ship | Layout A unlock | Starting loadout (A) | Unlock entity |
|---|---|---|---|
| Kestrel | Default | Burst Laser II + Artemis Missile; 3 humans; 8 reactor | — |
| Engi | Reach sector 5 with Kestrel | Ion Blast II + Anti-Ship Drone; 2 Engi + 1 human | — |
| Federation | Rebel shipyard event (Rebel Stronghold) or beat Flagship w/ Engi | Artillery Beam + Burst Laser I + Dual Lasers | `rebels` (faction) |
| Stealth | Engi fleet discussion event (Engi crew, Engi Homeworlds) | Mini Beam + Dual Lasers; no shields; Long-Range Scanners + cloak | `engi` (faction) |
<!-- SEQ-001: Engi crew + Engi Homeworlds (not Controlled) required. See `../dependencies.md` SEQ-001. -->
| Zoltan | Zoltan peace event -- hail, choose "without war" then "no bloodshed" | Halberd Beam + Ion Blast; 3 Zoltan; Zoltan Shield | `zoltan` (faction) |
| Mantis | Spare KazaaakplethKilik (Mantis Homeworlds; Mantis crew + Lv2 Medbay) | Small Bomb + Basic Laser; teleporter; Mantis crew | `mantis` (faction) |
| Slug | Slug unlock event | Dual Lasers + Breach Bomb I (AE) | `slug` (faction) |
| Rock | Rock unlock quest (survive solar flare, escort) | 2× Heavy Laser + Artemis; missile-heavy | `rock` (faction) |
| Crystal | Crystal chain (see below) OR beat Flagship w/ all A+B (excl. Lanius) | Crystal Burst I + Heavy Crystal I; Crystal Vengeance | `crystal` (crew) |
| Lanius | Unlock any 4 ships | Lanius B = Advanced Flak; suffocation-immune Lanius crew | `lanius` (crew) |

> Each unlock-event fact cross-routes to its faction/crew entity file. See `factions/` and `crew/` for the per-entity summaries; missable unlock steps are indexed in `sections/missables.md`.

## The Crystal Cruiser unlock chain

> The full step-by-step chain (the game's most complex missable sequence) is documented in `crew/crystal.md` and indexed in `sections/missables.md`. Summary: Damaged Stasis Pod → Zoltan research facility (revives Ruwen) → Ancient device in Rock Homeworlds → reach the Hidden Crystal Worlds. Hard bottleneck: Rock Homeworlds must appear by sector 7.

## Build archetypes

> See `mechanics.md` → "Builds / loadouts" for weapon-focused, drone-focused, boarding-focused, and hybrid/control archetypes and the recommended system-upgrade order.

## Sources
- ftl.fandom.com ship pages (community-wiki, captured 2026-06-02); Steam Community ship-unlock guides; Russian Steam ship-unlock guide; subagent
