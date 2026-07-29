# The Rebellion

**entity-id:** rebels
**class:** factions
**entity-status:** hostile
**entity-hidden:** no
**status:** research-integrated
**last_reconciled:** 2026-06-02

## Current status
The main antagonist faction. The **Rebel Pursuit Fleet** chases the player across every sector; **Rebel Controlled Sectors** are mid-late sectors the Rebels have taken over; the **Rebel Flagship** is the final boss in The Last Stand.

## Recruitment / Access (unlock event)
- The **Rebel shipyard** event in a **Rebel Stronghold** (sector 5+) shows a Flagship prototype under construction: destroy or crew-kill it to unlock the **Federation Cruiser**, delay the fleet 2 turns, and gain a free weapon. *(spoiler: progression.)*
- _source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com) · capture: web_fetch · confidence: medium · enemy-tier: 1 · puzzle-tier: 1 · category: mainline · spoiler: progression_ — [Confirmed: 3 sources]

## Combat -- the Rebel Pursuit Fleet
> `spoiler: none` for the pursuit mechanic itself (visible on the map from the start). Detailed advance-rate math (0x40/jump, nebula slowdowns, mercenary/Distraction-Buoys delays) lives in `mechanics.md` → "FTL drive & sector progression."

## Combat -- the Rebel Flagship (final boss)
> Gated at **enemy tier 2+** (`spoiler: late-game`). Full 3-phase breakdown, phase weapons, Power Surge behavior, and difficulty scaling live in `mechanics.md` → "The Rebel Flagship (final boss)." Summary: 3 phases in The Last Stand; jumps toward the Federation Base every 2 player jumps (3 base-jumps = loss); crew deaths persist between phases; the priority every phase is knocking out the missile launcher (~7 damage); Hacking + boarding trivialize it.
> **Cross-system dependency** -- see `../dependencies.md` DEP-012: Crew killed via boarding in Phase 1 stay dead in Phases 2 and 3; killing all crew makes the Flagship an un-boardable auto-ship.
- _source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com + Steam guides) · capture: web_fetch · confidence: medium · enemy-tier: 2 · puzzle-tier: 0 · category: mainline · spoiler: late-game_ — [Confirmed: 4-5 sources]

## See also
- `mechanics.md`; `factions/federation.md`; `sections/sector_types.md` (Rebel Controlled, Rebel Stronghold, The Last Stand).
