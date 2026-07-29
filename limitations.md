# FTL: Faster Than Light -- Limitations & Blocked Sources

Sources I found that look useful but couldn't fully fetch -- paywalls, Cloudflare, age gates, video-only content, etc. URLs preserved so the player (or another contributor) can open them in a real browser.

## How to read this file
- Each entry: topic, URL, block type, what I could glean, best alternative I did get to.
- Each per-topic file (in `items/`, `sections/`, `crew/`, `factions/`) also lists its own blocked sources at the bottom -- the player rarely needs to come hunting here.
- This file is the catch-all for sources that didn't fit a specific topic.

## Block types
- **paywall** -- content gated behind a subscription or article limit
- **cloudflare** -- Cloudflare bot challenge / 403 / 503 from WebFetch
- **video-only** -- YouTube or other video where the answer is shown visually; no readable text equivalent
- **age-gate** -- content blocked behind age verification
- **cookie-wall** -- popup or consent flow that broke the fetch
- **search-snippet-only** -- search engine returned a snippet but the page itself wasn't reachable
- **dead-link** -- URL was in another source but no longer resolves

## Entries

### P1 ingestion (2026-06-02) -- unresolved / unverified

- **Controls: full keyboard-remap list, controller support, accessibility rebinds** -- the P1 deep-research result did not surface a complete keyboard shortcut list, community-recommended remaps, or controller-support confirmation. Standard bindings carried from Stage 0 are in `controls.md`. Block type: research-gap (not a fetch block). Best alternative obtained: Steam page confirms mouse+keyboard + spacebar pause.
- **Settings: display/audio/colorblind** -- P1 did not cover resolution/fullscreen/multi-monitor behavior, audio mix, or whether FTL ships a colorblind mode. `settings.md` covers difficulty + AE toggle only. Block type: research-gap.
- **Distraction Buoys augment** -- exact store price/rarity not on the wiki Augmentations table; community estimate ~55 scrap / R3 (unverified). See `items/augmentations.md`.
- **Crystal-weapon stun% values** -- a few are single-sourced; verify. See `items/weapons.md`.
- **Achievement #40 ("Is it warm in here?") trigger mapping** -- single-sourced (community-wiki); verify the #40-vs-#15 distinction. See `achievements.md`.
- **Heavy Laser I stats** -- vanilla AE is 1 power / 9s charge; a popular balance MOD uses 2 power / 10s. Do not conflate. `items/weapons.md` carries the vanilla values.

### Corrections applied during P1 ingestion (recorded for audit)

- **Developer origin:** the P1 brief and Stage 0 stated "English (Canadian)." Corrected by the research enricher: Subset Games was founded in **Shanghai, China** by Justin Ma & Matthew Davis (former 2K China staff); working language is English. Applied to `architecture_manifest.md` (source-language set).
- **Lanius sector types:** the P1 brief's disambiguation rule 7 named three Lanius sector types ("Lanius Controlled Sector," "Lanius Homeworlds"). These do **not** exist as distinct AE event pools -- only the Abandoned Sector is the Lanius-themed type. Applied to `architecture_manifest.md`, `sections/sector_types.md`, `factions/lanius.md`. The `sections/index.md` scaffold's "Lanius Controlled/Homeworlds" row is superseded.
- **Weapon types:** Stage 0 said 6 weapon types / ~30+; corrected to **7 types / 40+** (flak and crystal are distinct). Applied to `items/`.

## Always-blocked categories

- **Procedurally generated run outcomes** -- per-run event sequences, enemy spawn tables per beacon, and specific loot drops are randomized; no source documents individual run outcomes. Guidance covers system mechanics, known event patterns, and probability data where available.
- **Fandom wiki (ftl.fandom.com)** -- Cloudflare-gated from automated fetch. Content available via manual browser session; key pages should be transcribed and ingested into the corpus directly. Stage 0 used Wikipedia and Steam descriptions instead.
