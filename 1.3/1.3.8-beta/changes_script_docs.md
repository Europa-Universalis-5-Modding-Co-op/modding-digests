# Script Documentation 1.3.8-beta
## Table of Contents
 * [Triggers](#triggers)
 * [On Actions](#on-actions)
## Notes
 * **Changed** means the description, scopes or anything related to the documentation for this element has changed
 * The list of iterators do **not** include generated geographic region based iterators
 * The on action scope is based on the script documentation, for more information see the `common/on_actions` directory

## Triggers
| Type | Trigger | Trait | Description |
|--|--|--|--|
| Added | `average_control` | Value | Checks the average control in the country |
| Added | `current_day` | Value | Compare the current ingame day (1..31) |
| Added | `has_ai_disposition_toward` |  -  | Does the scope country view the target country with the given AI disposition? Usage: has_ai_disposition_toward = { target = \<country link\> disposition = \<alarmed/wary/planning_war/covets/domineering/rivals/indifferent/friendly\> } |
| Added | `has_game_started` | Boolean | Has the game started? |
| Removed | `military_tech_level` | Value | Checks if a country has a certain level of military tech |

## On Actions
| Type | On Action | Scope |
|--|--|--|
| Added | `on_pre_war_declared` | `none` |
