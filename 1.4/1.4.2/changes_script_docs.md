# Script Documentation 1.4.2 - beta
## Table of Contents
 * [Triggers](#triggers)
 * [Modifiers](#modifiers)
## Notes
 * **Changed** means the description, scopes or anything related to the documentation for this element has changed
 * The list of iterators do **not** include generated geographic region based iterators
 * The on action scope is based on the script documentation, for more information see the `common/on_actions` directory

## Triggers
| Type | Trigger | Trait | Description |
|--|--|--|--|
| Added | `has_proximity_source_building` | Boolean | Check if a location holds a building that grants local_proximity_source |
| Added | `is_historical_capital` | Boolean | Check if a location is a historical capital of its owner |
| Changed | `loyalty_from_subject_bloc_strength` | Value | Checks the loyalty change all subjects as a bloc would cause for a subject of the given type. Usage: loyalty_from_subject_bloc_strength = { type = \<subject type\> value \<operator\> \<value\> } or loyalty_from_subject_bloc_strength(\<subject type\>) |

## Modifiers
| Type | Modifier | Scope |
|--|--|--|
| Added | `local_proximity_source_modifier` | Location |
