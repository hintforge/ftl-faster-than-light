# FTL: Faster Than Light -- Ship Systems

**status:** research-integrated
**last_reconciled:** 2026-06-02

Systems are permanently installed modules with upgradeable levels, powered from the reactor. Values are vanilla Advanced Edition. Reactor-level power math and the absolute max-power figure live in `mechanics.md` ("Power management").

_source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com systems pages + subagent) · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_ — applies to the table. [Confirmed: subagent + wiki]

| System | Function | Levels | Power | Acquisition | Build notes |
|---|---|---|---|---|---|
| Shields | Each 2 power = 1 bubble (blocks 1 shot) | 1-8 (4 bubbles at L8) | 2/bubble | Start on most; ~125 scrap | Top priority; 2 bubbles by S3. |
| Engines | Evasion + FTL charge rate | 1-8 (+5%/bar) | 1/bar | Start on all | Aim 40-45% evade. |
| Weapons | Powers weapons | 1-8 | varies | Start on all | Power your loadout. |
| Oxygen | Refills ship O2 | 1-3 | 1 | Start on all | Rarely upgrade. |
| Medbay | Heals crew in room | 1-3 | 1-3 | Start on most | On-demand heal; blue events. |
| Clone Bay (AE) | Revives dead crew on jump (skill loss) | 1-3 | 1-3 | Swaps with Medbay | Boarding builds; no mid-fight heal. |
| Piloting | Evasion (autopilot) + FTL | 1-3 | subsystem | Start on all | L2/L3 = 50%/80% autopilot evade. |
| Sensors | Reveals enemy interior | 1-3 | subsystem | Start on most | Useless in nebula. |
| Doors | Blast doors vs boarders/fire | 1-4 | subsystem | Start on all | L3-4 vital vs boarders. |
| Teleporter | Sends boarders | 1-3 | 1 | Buy/start | L2 recharge before suffocation; L3 spam. |
| Cloaking | +60% evade; stops enemy weapon charge | 1-3 | 1 | Buy ~150 | Best defense; time vs missiles. |
| Hacking (AE) | Disables 1 enemy system 4/7/10s | 1-3 | 1-3 | Buy | Hack shields/weapons; carries weak builds. |
| Mind Control (AE) | Controls enemy crew 14/20/28s | 1-3 | 1-3 | Buy | Counter boarders; flip enemy pilot. |
| Artillery: Burst/Ion/Beam/Flak | Auto-firing pierce weapon (Fed) | 1-4 | own room | Fed A (Beam), Fed B, Fed C (Flak) | Pierces all shields; charge 50→20s. |
| Backup Battery (AE) | +2/+4 temp power 30s, 20s cooldown | 1-2 | subsystem | Buy/start | Power swings; ion-immune. |
| Drone Control | Powers drones | 1-8 | varies | Buy/start | Defense Drone I alone justifies it. |

## Notes
- **Medbay and Clone Bay are mutually exclusive** -- a ship cannot install both.
> **Cross-system dependency** -- see `../dependencies.md` DEP-003: Clone Bay and Medbay cannot coexist; Engi Med-bot Dispersal healing also stops working with Clone Bay.
- **Artillery Beam** (Federation A/B) pierces ALL shields, deals 1 dmg/room, charges 50/40/30/20s by level, draws from its own room power (not Weapons), and never misses.
- Detailed per-system mechanics (Hacking durations, Mind Control immunities, Cloaking timing, Clone Bay skill-loss) live in `mechanics.md`.

## Sources
- ftl.fandom.com systems pages (community-wiki, captured 2026-06-02); subagent cross-check; community upgrade-priority guides
