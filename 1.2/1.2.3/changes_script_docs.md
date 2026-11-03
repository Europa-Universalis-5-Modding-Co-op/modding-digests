# Script Documentation 1.2.2 and 1.2.3
## Table of Contents
 * [Triggers](#triggers)
 * [Modifiers](#modifiers)
## Notes
 * **Changed** means the description, scopes or anything related to the documentation for this element has changed
 * The list of iterators do **not** include generated geographic region based iterators
 * The on action scope is based on the script documentation, for more information see the `common/on_actions` directory

## Triggers
| Type    | Trigger       | Trait   | Description                           |
| ------- | ------------- | ------- | ------------------------------------- |
| Changed | `has_spawned` | Boolean | Has the institution spawned anywhere? |

## Modifiers
| Modififcation Type | Modifier                                        | Description |
| ------------------ | ------------------------------------------------| ----------- |
| Added              | add_religious_aspect_hellenism_cost_modifier    |             |
| Added              | change_religious_aspect_hellenism_cost_modifier |             |
| Added              | remove_religious_aspect_hellenism_cost_modifier |             |