# Changelog

All notable changes to this project will be documented in this file.

## [1.3.0] - 2026-08-14

- The Viltrumite portraits ship with the mod. 28 portraits are selectable under the Viltrumite species class in the empire creator, alongside the human set for a Viltrumite passing as one
- The Viltrum Empire and Thragg now use a Viltrumite portrait by default instead of a human one
- The species class name reads correctly in ten languages

## [1.2.0] - 2026-08-14

- Verified against **Stellaris 4.4.6 "Pegasus"**; `descriptor.mod` now reports `4.4.6`
- The Scourge Virus chain now runs. Its opening event reached for the capital as a planet, but a capital is a colony scope, so the chain silently stopped before the first pop died
- The **Embedded Viltrumite** operation now loads. It sat in `common/espionage_operations/`, which the game does not read, and was missing its `stages` count and a valid resource category
- Its three stages are now `espionage_operation_event`, the only event type an operation stage fires, and the world it seizes changes hands on the final stage — the old `on_success` block was not a field the game recognises
- Corrected three modifiers the game silently ignored: the Viltrum Survivors ruler-skill and vassal naval-capacity bonuses, and the Sequid slave political-power bonus
- Added the generated-species names the Viltrumite species class requires
- Saved the name lists as UTF-8 with BOM, the encoding Stellaris expects

## [1.1.0] - 2026-07-08

- Updated for **Stellaris 4.4 "Pegasus"** — `descriptor.mod` now targets `v4.4.*`
- Added an embedded-agent espionage operation (`common/espionage_operations/`), its static modifiers (`common/static_modifiers/`), and espionage events (`events/viltrum_espionage_events.txt`)
- Major **Viltrum Survivors** origin rework: greatly increased ship-combat, economy, and research bonuses
- Rebalanced the **Pure Viltrumite** trait: 10000% army damage & health, added army morale
- Set the Pure Viltrumite population-growth penalty to **-50%** (superseding the -95% from 1.0.4)
- Tweaked Coalition and Thraxxan origins and the Coalition trait
- Refreshed event pictures and English localisation

## [1.0.4] - 2026-04-03

- Increased the population growth penalty for the Viltrumite Pure trait from -50% to -95%, making expansion near-zero to better balance the trait's extreme power bonuses

## [1.0.3] - 2026-04-03

- `localisation/english/viltrumite_l_english.yml` — the localisation fix
- `public/nit.json` — version metadata

## [1.0.2] - 2026-04-03

- viltrum-empire Release v1.0.2

## [1.0.1] - 2026-04-03

- viltrum-empire Release v1.0.1

