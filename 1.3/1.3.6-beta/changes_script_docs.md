# Script Documentation 1.3.6-beta
## Table of Contents
 * [Triggers](#triggers)
 * [Event Targets](#event-targets)
 * [Modifiers](#modifiers)
## Notes
 * **Changed** means the description, scopes or anything related to the documentation for this element has changed
 * The list of iterators do **not** include generated geographic region based iterators
 * The on action scope is based on the script documentation, for more information see the `common/on_actions` directory

## Triggers
| Type | Trigger | Trait | Description |
|--|--|--|--|
| Added | `has_ai_disposition_toward_actor` |  -  | Does the country view scope:actor with the given AI disposition? Used by the disposition map mode to color by the selected country's perspective; scope:actor falls back to the player when nothing is selected. (alarmed/wary/planning_war/covets/domineering/rivals/indifferent/friendly) |
| Changed | `country_interaction_acceptance` | Value | How high is the target country's AI value of accepting the country interaction done by the current country scope? Always return 0 if the country interaction has no acceptance   |
| Changed | `has_ai_disposition_toward_player` |  -  | Does the country view the player with the given AI disposition? (alarmed/wary/planning_war/covets/domineering/rivals/indifferent/friendly) |
| Changed | `reverse_country_interaction_acceptance` | Value | How high is the current country's AI value of accepting the country interaction done by the specified country scope? Always return 0 if the country interaction has no acceptance   |

## Event Targets
| Type | Event Target | Description |
|--|--|--|
| Added | `ai_best_proximity_candidate` | gets the best proximity candidate location |

## Modifiers
| Type | Modifier |
| -- | -- |
| Added | `ai_amount_of_parallel_charters` |
| Added | `ai_conquer_desire_religion_mult` |
