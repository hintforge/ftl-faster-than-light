# FTL: Faster Than Light -- Game Guide
<!-- v1 -- 2026-06-02 00:00 UTC -->
<!-- forged with hintforge v65 · CC BY-NC-SA 4.0 -->

This folder is a spoiler-controlled reference for the player's FTL: Faster Than Light playthrough. It is **not** a Claude Code task list. AI agent sessions opened here read this file for orientation, then look up specific topics in the subfolders below.

## Hard rules
- **Spoiler-free unless tier raised.** No story beats, no enemy reveals, no encounter telegraphs. (See `warning_tiers.md`.)
- **PC / Steam (mouse+keyboard).** Translate any other-platform references before quoting.
- **Hint ladder for sector events and tactical decisions.** Smallest nudge first; escalate on request.
- **Don't invent solutions.** If no source has it, say so and link the closest source.
- **Every claim cites a source** in the structured form (see `../../hintforge/templates/claim_format.md`).
- **Procedural roguelike.** Each run generates a new galaxy; per-run outcomes are not pre-documented. Guidance covers systems, weapons, build strategies, and known event patterns -- not individual run state.

## Folder map
- `CHECKPOINT.md` -- current playthrough state. Read first for context.
- `mechanics.md` -- core game-system rules: combat, power management, FTL drive, crew mechanics, fire/breach, weapon interactions, sector progression. Stable cross-run knowledge surface.
- `limitations.md` -- sources I couldn't fully access; URLs preserved.
- `crew/` -- crew species traits, skill progression, and role optimization. `index.md` is the roster.
- `factions/` -- alien races and faction behaviors (Engi, Mantis, Rock, Slug, Zoltan, Crystal, Lanius, Federation, Rebels). `index.md` is the roster.
- `items/` -- weapons / drones / augmentations / systems upgrades, split by category.
- `sections/` -- sector-type notes, missable event callouts, story beats.
- `persona.md` -- voice configuration (currently plain assistant).
- `warning_tiers.md` -- enemy & puzzle tier flags. Check before any preemptive info.

## Workflow
- When the player starts a new run or reaches a significant milestone, update `CHECKPOINT.md`.
- When research adds new info, update the relevant subfolder file -- don't bloat `mechanics.md`.
- Every fact: structured-claim form with source + confidence.

> Framework: `../../hintforge/`. See `../../hintforge/principles.md` for the full rule set, `../../hintforge/templates/claim_format.md` for source-citation conventions, `../../hintforge/ingestion.md` when the user says "ingest the research" (cascade result integration; runs in a fresh session), and `../../hintforge/stitch_and_zipper.md` when the user says "run stitch" or "run zipper" (post-ingestion synthesis; runs in a fresh session).
