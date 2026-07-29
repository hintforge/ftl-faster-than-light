# FTL: Faster Than Light -- Crew

**status:** research-integrated
**last_reconciled:** 2026-06-02
**class:** crew

## Why this file exists

The corpus's roster for FTL's crew species. FTL crew are run-bound role-fillers (Pilot, Gunner, Engineer, Medbay, etc.) whose species determines passive bonuses; crew skill levels up through use, and deaths within a run are permanent. The reader consults this file for crew-shaped questions ("what species pilots best," "what does Lanius crew do," "which crew heals fastest").

## Roster (8 species)

| entity-id | display name | first-encounter zone | missable | per-species file |
|---|---|---|---|---|
| human | Human | civilian_starting (starting crew) | no | `crew/human.md` |
| engi | Engi | engi_controlled | no | `crew/engi.md` |
| zoltan | Zoltan | zoltan_controlled | no | `crew/zoltan.md` |
| mantis | Mantis | mantis_controlled | no | `crew/mantis.md` |
| rock | Rock | rock_controlled | no | `crew/rock.md` |
| slug | Slug | slug_controlled_nebula | no | `crew/slug.md` |
| crystal | Crystal | hidden_crystal_worlds (event chain) | **yes** | `crew/crystal.md` |
| lanius | Lanius | abandoned_sector (AE only) | no | `crew/lanius.md` |

## Species stat table

_source: P1 deep-research cascade 2026-06-02 (ftl.fandom.com + JP iphoneac.com datamining) · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_ — [Confirmed: datamining]

| Species | HP | Move | Combat | Repair | Notable trait |
|---|---|---|---|---|---|
| Human | 100 | 1.0× | 1.0× | 1.0× | ~10% faster skill leveling; no other trait |
| Engi | 100 | 1.0× | 0.5× | 2.0× | Best repair; weak melee |
| Mantis | 100 | 1.2× | 2.0× | 0.5× | Best boarder/defender; poor firefighter |
| Rock | 150 | 0.5× | 1.0× | 1.0× | Fire-immune; tanky; slow |
| Zoltan | 70 | 1.0× | 0.5× | 1.0× | +1 free power to occupied system; 15-dmg+ion death burst; ion-proof power |
| Slug | 100 | 1.0× | 1.0× | 1.0× | Sees crew/rooms without sensors; mind-control immune |
| Crystal | 125 | 0.5× | 1.0× | 1.0× | Lockdown power (~10s); 0.5× suffocation damage |
| Lanius (AE) | 100 | 0.8× | 1.0× | 1.0× | Suffocation-immune; drains room O2; mind-control immune; slow |

## Crew mechanics (cross-species)
- Untrained human repairs 1 system bar or seals 1 breach in 12.5s. Firefighting uses repair speed -- a lone Mantis is "nearly worthless" at it.
- Only manned-station skills (Piloting/Shields/Engines/Weapons) credit XP while manning. Mantis combat threshold 7 vs human 8.
- Dying-animation times (affect cloning / crew-kill timing): Rock/Crystal/Engi 2s; Human/Slug/Lanius 1.8s; Mantis 1.7s; Zoltan 1.5s.
- _source: P1 deep-research cascade 2026-06-02 (datamining) · capture: web_fetch · confidence: medium · enemy-tier: 0 · puzzle-tier: 0 · category: mainline · spoiler: none_ — [Confirmed: datamining + 2 sources]

## Crystal crew event chain
The Crystal crew are recruitable only via a missable multi-step chain (required for "Ancestry"). Full chain documented in `crew/crystal.md`; indexed in `sections/missables.md`.

## Sources
- ftl.fandom.com crew species pages (community-wiki, captured 2026-06-02); Japanese iphoneac.com data tables; community tier-list discussions.
