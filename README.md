# FTL: Faster Than Light — Hintforge Companion

![FTL companion status — coverage, how current it is, and spoiler control](assets/readme-status-card.svg)

A spoiler-controlled hint companion for **FTL: Faster Than Light**, the spaceship-management roguelike where you run one ship ahead of a pursuing fleet, one jump at a time. Built in the [Hintforge](https://github.com/hintforge/builder) format: a loyal sidekick that answers only from these guide files — never from guesswork — at the spoiler level you set.

## Use it

You need a Hintforge reader running in Claude Code, Codex, or OpenClaw. Point it at this repo:

> Load the FTL guide from github.com/hintforge/ftl-faster-than-light

Then just ask — *"how do I fit this loadout," "what beats a Zoltan shield," "how do I win the flagship."* Runtime setup lives in [`hintforge/reader`](https://github.com/hintforge/reader).

## Spoilers

**You** set two independent dials — enemy warnings (Tier 0–5) and event/puzzle warnings (Tier 0–3) — both **silent by default**; the guide volunteers nothing until you raise one. Specific event outcomes are spoiler-tiered even though the underlying mechanics aren't. There's no save-state reader (FTL's save is binary), so every answer comes from this guide's files.

## What's inside

A structured Markdown corpus — ship systems and combat mechanics, crew races, weapons and drones, sector/faction events, and all achievements. Interactive tools (a ship-loadout / power-grid simulator is the obvious fit) aren't built yet. The companion reads and writes only the files you control.
