# FTL: Faster Than Light

![FTL companion status: coverage, how current it is, and spoiler control](assets/readme-status-card.svg)

![Power allocation scratchpad built on this corpus: reactor power split across every ship system, each row carrying the corpus reference figure, a flag when an entry runs past it, a running allocated-versus-available total, and a free-text note for your own reasoning](assets/readme-power-planner.png)

A free hint guide for FTL: Faster Than Light, with spoilers kept at the level you choose. Get help with this spaceship-management roguelike as you stay ahead of a pursuing fleet, one jump at a time. Your AI agent answers only from the guide files.

## Use it

Install the [reader](https://github.com/hintforge/reader) in any AI agent that can read files on your computer, then tell it:

> Load the FTL guide from github.com/hintforge/ftl-faster-than-light

Try "how do I fit this loadout", "what beats a Zoltan shield" or "how do I win the flagship".

The guide uses the [Hintforge](https://github.com/hintforge/builder) format. The agent reads and writes only files you control.

## Spoilers

Enemy warnings (Tier 0 to 5) and event or puzzle warnings (Tier 0 to 3) start silent. The guide volunteers nothing until you raise a dial. Specific event outcomes have spoiler levels; underlying mechanics don't.

There is no save reader because FTL's save is binary.

## What's inside

- Ship systems, combat mechanics and crew races.
- Weapons, drones, sector and faction events, and all achievements.

## Power planner

Open [`artifacts/power_planner.html`](artifacts/power_planner.html) in any browser. It needs no account, installation or AI. The scratchpad totals reactor allocations, flags systems above guide reference figures, notes incompatible systems and saves your plan locally.

It checks arithmetic. It doesn't verify what your game version allows.
