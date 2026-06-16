# Script Documentation 1.3.4-beta
## Table of Contents
 * [Effects](#effects)
 * [Triggers](#triggers)
## Notes
 * **Changed** means the description, scopes or anything related to the documentation for this element has changed
 * The list of iterators do **not** include generated geographic region based iterators
 * The on action scope is based on the script documentation, for more information see the `common/on_actions` directory

## Effects
| Type | Effect | Description |
|--|--|--|
| Added | `add_recovered_army_levy_percentage` | adds recovered land levies into the province based on percentage |
| Added | `add_recovered_navy_levy_percentage` | adds recovered naval levies into the province based on percentage |
| Changed | `end_situation` | End a situation |

## Triggers
| Type | Trigger | Trait | Description |
|--|--|--|--|
| Added | `available_army_levy_percentage` | Value | Checks the percentage of available army levies |
| Added | `available_navy_levy_percentage` | Value | Checks the percentage of available naval levies |
| Added | `province_army_levy_percentage` | Value | Percentage of army levies that can be raised from a province |
| Added | `province_navy_levy_percentage` | Value | Percentage of naval levies that can be raised from a province |

## Modifiers
| Type | Modifier |
| -- | -- |
| Added | `harmony_stability` |
