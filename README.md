<p align="center">
  <img src="thumbnail.png" width="360" alt="Viltrum Empire" />
</p>

<h1 align="center">Viltrum Empire</h1>

<p align="center">
  <b>A total-conversion Stellaris mod that drops the <em>Invincible</em> universe into the galaxy.</b>
</p>
<p align="center">
  Seven canon factions, an asymmetric lore-accurate balance, and event chains<br />
  that cull the Viltrumite race and shatter worlds to debris.
</p>

<p align="center">
  <a href="https://steamcommunity.com/sharedfiles/filedetails/?id=3602982845"><img src="https://img.shields.io/badge/Steam_Workshop-Subscribe-2563eb?style=for-the-badge&logo=steam&logoColor=white" alt="Steam Workshop" /></a>
  <img src="https://img.shields.io/badge/Stellaris-v4.4-2563eb?style=for-the-badge&logo=steam&logoColor=white" alt="Stellaris v4.4" />
  <img src="https://img.shields.io/badge/Total_Conversion-Invincible_Universe-3b82f6?style=for-the-badge" alt="Total Conversion" />
  <img src="https://img.shields.io/badge/Factions-7_playable-1f56cf?style=for-the-badge" alt="7 factions" />
  <img src="https://img.shields.io/badge/license-Proprietary-1f56cf?style=for-the-badge" alt="License" />
</p>

<br />

## Why Viltrum Empire

Most empire packs hand you a fresh flag and the same balanced stat spread as everyone else. This mod does the opposite: it rebuilds seven *Invincible* factions from canon, then lets that canon dictate the numbers. The Viltrumites are so absurdly strong that they can barely reproduce; the GDA can only dig in and endure; and a start-of-game plague and a world-shattering bombardment stance make sure the fantasy plays out mechanically, not just in the flavor text.

<table width="100%">
  <tr>
    <td width="33%" valign="top">
      <h3 align="center">Play the Invincible universe</h3>
      <p align="center">Seven canon factions — Viltrumites, GDA, Thraxxans, Coalition, Sequids, Flaxans, and Martians — ship as playable species and ready-made empires.</p>
    </td>
    <td width="33%" valign="top">
      <h3 align="center">Asymmetric by design</h3>
      <p align="center">Balance is derived from canon, not min-maxing. The Pure Viltrumite trait grants 10000% army damage and near-immortal leaders, offset by -50% population growth — you conquer instead of grow.</p>
    </td>
    <td width="33%" valign="top">
      <h3 align="center">Signature event chains</h3>
      <p align="center">A Scourge Virus cull leaves roughly 100 elite survivors at game start, and a custom bombardment stance shatters worlds to debris at maximum devastation.</p>
    </td>
  </tr>
</table>

<br />

## Install

**Steam Workshop (recommended)** — [Subscribe on the Workshop](https://steamcommunity.com/sharedfiles/filedetails/?id=3602982845), launch Stellaris, and enable **Viltrum Empire** in the launcher's mod list.

**Manual** — place this mod folder inside your Stellaris `mod` directory so the launcher reads its `descriptor.mod`, then enable it in the launcher's playset:

| OS | Mod directory |
| :--- | :--- |
| Windows | `%USERPROFILE%\Documents\Paradox Interactive\Stellaris\mod\` |
| macOS | `~/Documents/Paradox Interactive/Stellaris/mod/` |
| Linux | `~/.local/share/Paradox Interactive/Stellaris/mod/` |

This is a **total conversion** built for **Stellaris v4.4** (per `descriptor.mod`). It reworks core content and is not intended to run alongside other major overhaul mods.

## Usage

Start a new game and pick one of the seven prescripted empires, or build your own using the mod's species and traits. Each empire pairs a species with its own authority, ethics, civics, custom origin, and ruler.

| Empire | Species | Ruler | Identity |
| :--- | :--- | :--- | :--- |
| **Viltrum Empire** | Viltrumites | Grand Regent Thragg | Dictatorial xenophobe-militarist on the **Viltrum Survivors** origin |
| **Global Defense Agency** | Humans | Director Cecil Stedman | Earth's defensive establishment — research and fortify to hold the line |
| **Thraxxan Hive** | Thraxxans | Thraxxan Queen | Its own strategic niche and trait set |
| **Coalition of Planets** | Coalition Species | Thaedus | Its own strategic niche and trait set |
| **Sequid Consciousness** | Sequids | Prime Sequid | Its own strategic niche and trait set |
| **Flaxan Empire** | Flaxans | Flaxan Emperor | Its own strategic niche and trait set |
| **Martian Confederacy** | Martians | Commander Levy | Its own strategic niche and trait set |

### What each species plays like

Every faction has one bespoke species-trait file, so no two play alike:

| Trait | Belongs to | What it does |
| :--- | :--- | :--- |
| **Pure Viltrumite** | Viltrumites | +5,000 leader lifespan, 10000% army damage & health, +30% research speed, +25% edict fund, perfect habitability — all offset by **-50% population growth** |
| **GDA Training** | Humans | +10% engineering research, +10% ship hull & hull regen, +2 defense platform capacity, +5% happiness, +10% unity — a fortify-and-hold defense game |

The **Viltrumites** are the dominant warrior race: superhuman combat stats and a 5,000-year lifespan that mirror their canonical invincibility, but they can barely grow. The **Global Defense Agency**'s humans lean on engineering and durability to survive. The remaining five factions each fill a distinct niche with their own trait file and per-species name list.

### The two event chains

Both chains are wired through custom `on_actions` and back their pop-ups with six bespoke event pictures:

- **Scourge Virus** (`viltrum_start_pops`) fires at game start for Viltrum Survivors empires, culling the population from billions down to roughly 100 elite pure-blooded survivors — the mechanical reason Viltrumites must conquer rather than expand.
- **Planet annihilation** (`viltrum_annihilation`) pairs the **Viltrumite Annihilation** bombardment stance (15x planet damage, only for the Viltrum Survivors origin) with an event that converts any world reaching **99% devastation** into uninhabitable shattered debris.

## How it works

- **Canon drives the numbers.** Each faction is one species definition plus one trait file, tuned to its *Invincible* portrayal rather than to a balanced curve — extreme highs paid for with extreme lows.
- **Prescripted empires are self-contained.** The seven files in `prescripted_countries/` bind a species to its authority, ethics, civics, origin, flag, and ruler, so they spawn ready to play (and as AI opponents).
- **Origins gate the mechanics.** The **Viltrum Survivors** origin is what unlocks the Scourge Virus start and the annihilation bombardment stance; only empires on that origin get them.
- **Presentation is native.** All player-facing text lives in one English localisation file with Stellaris color-coded tooltips, backed by a custom Viltrumite species class, portrait set, and a bespoke Viltrum flag with a map-mode variant.

## Mod structure

```
descriptor.mod              Mod metadata (name, version, Workshop id, tags)
thumbnail.png               Workshop thumbnail
common/
  species/                  7 species definitions
  traits/                   7 species trait files + shared leader traits
  governments/civics/       7 faction origin/civic files (incl. Viltrum Survivors)
  name_lists/               7 per-species name lists
  species_classes/          Custom VILTRUMITE species class
  portrait_sets/            Viltrumite portrait mapping
  on_actions/               Event triggers
  bombardment_stances/      Viltrumite annihilation stance
  espionage_operations/     Embedded-agent infiltration operation
  static_modifiers/         Espionage operation modifiers
events/                     Scourge Virus, planet annihilation + espionage events
prescripted_countries/      7 playable prescripted empires
flags/viltrum/              Custom Viltrum flag (+ map-mode variant)
gfx/event_pictures/         Event picture textures
interface/                  Event picture sprite definitions
localisation/english/       English strings and tooltips
```

## License

Proprietary — Copyright (c) 2026 Trenton Taylor. All rights reserved. No permission is granted to use, copy, modify, or distribute the software. See [LICENSE.md](LICENSE.md).

<br />

<p align="center">
  <sub>Seven factions, one galaxy — conquer it as the race too strong to grow.</sub>
</p>
