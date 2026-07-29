# FTL: Faster Than Light -- Augmentations

**status:** research-integrated
**last_reconciled:** 2026-06-02

Augmentations are passive ship bonuses. **Maximum 3 per ship.** Format below: name (scrap price, rarity, AE-flag where noted) -- effect. Values are vanilla Advanced Edition.

_source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com Augmentations page + subagent) · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_ — applies to all lists below. [Confirmed: subagent + wiki]

## Offensive
- **Automated Re-loader** (40, R2) -- +10% weapon fire rate, stacks, works while Weapons damaged.
- **Defense Scrambler** (80, R4, AE) -- blocks enemy defense/anti-combat drones.
- **Explosive Replicator** (60, R3, AE) -- 50% chance not to consume a missile.
- **Hacking Stun** (60, R3, AE) -- hacked systems' rooms stun crew.
- **Stealth Weapons** (50, R3) -- fire without breaking cloak.
> **Cross-system dependency** -- see `../dependencies.md` DEP-011: Stealth Weapons is required to fire during Cloaking; without it, any weapon fired immediately cancels the cloak.
- **Weapon Pre-Igniter** (120, R4) -- weapons fully charged after a jump (does NOT fully charge Chain Vulcan/Glaive -- one charge only).
> **Cross-system dependency** -- see `../dependencies.md` DEP-006: Pre-Igniter gives charge weapons only one charge after a jump; Chain Vulcan and Glaive Beam are not fully ready on the first post-jump shot.
- **Zoltan Shield Bypass** (55, R3, AE) -- teleport/mind-control through Zoltan Super Shields.
> **Cross-system dependency** -- see `../dependencies.md` DEP-008: Zoltan Shield Bypass is the only way to use Teleporter or Mind Control through an enemy Zoltan Super Shield.

## Defensive
- **Fire Suppression** (65, R3, AE) -- auto-extinguishes all fires.
- **Repair Arm** (50, R3) -- +2 hull per scrap pickup, but −15% scrap.
- **Reverse Ion Field** (45, R2) -- 50% ion negate, stacks to immunity.
- **Shield Charge Booster** (45, R2) -- +15% shield recharge rate (×1.45 multiplier), works while Shields damaged.

## Crew
- **Backup DNA Bank** (40, R2, AE) -- keeps the Clone queue if the Clone Bay is powered off.
- **Emergency Respirators** (50, R2, AE) -- half O2 (suffocation) damage.
- **Reconstructive Teleport** (70, R3, AE) -- teleporting crew back fully heals them.

## FTL / Navigation
- **Advanced FTL Navigation** (50, R3) -- jump to any previously-visited beacon.
- **Distraction Buoys** (AE) -- delays the Rebel fleet 1 jump at sector start. *(Exact store price/rarity not on the wiki table; community cites ~55 scrap, R3 -- unverified.)*
- **FTL Jammer** (30, R3) -- doubles enemy jump time.
- **FTL Recharge Booster** (50, R2) -- ×0.80 FTL charge time, stacks.

## Utility
- **Battery Charger** (40, R2, AE) -- halves Backup Battery cooldown.
- **Drone Recovery Arm** (50, R2) -- recovers external drones.
- **Lifeform Scanner** (40, R3, AE) -- sense all crew (incl. through nebula).
- **Long-Range Scanners** (30, R1) -- reveal adjacent-beacon hazards/ships; starts on all Stealth Cruisers.
- **Scrap Recovery Arm** (50, R1) -- +10% scrap from all sources (not from selling).

## Ship-specific (with sell value)
Each is the defining augment of its associated species/ship; can be sold.
- **Crystal Vengeance** (40) -- 10% chance to fire a shard back when hit. (Triggers the "Sweet Revenge" achievement.) -- `entity: crystal` (crew)
> **Cross-system dependency** -- see `../dependencies.md` DEP-007: Crystal Vengeance is the sole trigger for achievement #46 Sweet Revenge; the achievement requires killing an enemy with the counter-shard.
- **Mantis Pheromones** (25) -- +25% crew movement speed. -- `entity: mantis` (crew)
- **Rock Plating** (40) -- 15% chance to negate hull damage. -- `entity: rock` (crew)
- **Slug Repair Gel** (30) -- auto-repairs all breaches. -- `entity: slug` (crew)
- **Titanium System Casing** (40) -- 15% chance to negate system damage.
- **Zoltan Shield** (40) -- 5-HP Super Shield on arrival at each beacon. -- `entity: zoltan` (crew)
- **Engi Med-bot Dispersal** (30) -- heals crew outside the Medbay (does not work with a Clone Bay). -- `entity: engi` (crew)
> **Cross-system dependency** -- see `../dependencies.md` DEP-003: Clone Bay and Medbay are mutually exclusive; Med-bot Dispersal healing is disabled when Clone Bay is installed.
- **Drone Reactor Booster** (25) -- +25% crew-drone speed.

## Sources
- ftl.fandom.com Augmentations page (community-wiki, captured 2026-06-02); subagent cross-check

### Unverified for this file
- Distraction Buoys exact price/rarity not displayed on the wiki Augmentations table; community estimate ~55 scrap / R3. [flag]
