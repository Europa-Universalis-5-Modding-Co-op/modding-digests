# Script Documentation 1.4.1 - Beta
## Table of Contents
 * [Effects](#effects)
 * [Triggers](#triggers)
 * [On Actions](#on-actions)
## Notes
 * **Changed** means the description, scopes or anything related to the documentation for this element has changed
 * The list of iterators do **not** include generated geographic region based iterators
 * The on action scope is based on the script documentation, for more information see the `common/on_actions` directory

## Effects
| Type | Effect | Description |
|--|--|--|
| Added | `reroll_parliament_agendas` | Re-roll the parliament agenda of every estate currently participating in the parliament.  |
| Added | `set_show_stats` | Shows or hides the character's adm/dip/mil abilities in the UI. Hidden abilities still count for gameplay and AI |
| Changed | `create_character` | Creates a character for a country. The effect has the following parameters:   |
| Changed | `declare_war_with_cb` | declares a war with a specific cb  { target = \<country\> type = \<cb_type\> \[target_province = ; target_country =, character =, apply_declaration_costs = yes\] } The country scope will leave all wars they fight together with the target country. apply_declaration_costs makes the war cost what a normal declaration costs - stability, war exhaustion, antagonism, trust, truce breaking and one diplomat - and defaults to no, so gate the caller on num_of_diplomats yourself. |

## Triggers
| Type | Trigger | Trait | Description |
|--|--|--|--|
| Added | `has_parliament_agendas` | Boolean | Checks if at least one participant in the parliament is currently pushing an agenda |
| Added | `is_valid_goal_for_charter` |  -  | Whether this colonial charter goal is available for the given colonial charter. The null goal (automatic) is always valid |
| Added | `num_open_cabinet_positions` | Value | Checks if a country has a certain amount of open cabinet positions |
| Added | `shows_stats` | Boolean | character's adm/dip/mil abilities are shown in the UI |

## Modifiers
| Type | Modifier | Scope |
|--|--|--|
| Added | `reroll_parliament_agendas_cost_modifier` | Country |

## On Actions
| Type | On Action | Scope |
|--|--|--|
| Added | `on_colonial_charter_finished` | `country` |

