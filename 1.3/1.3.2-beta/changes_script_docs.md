# Script Documentation 1.3.2-beta
## Table of Contents
 * [Triggers](#triggers)
## Notes
 * **Changed** means the description, scopes or anything related to the documentation for this element has changed
 * The list of iterators do **not** include generated geographic region based iterators
 * The on action scope is based on the script documentation, for more information see the `common/on_actions` directory
## Triggers
| Type | Trigger | Trait | Description |
|--|--|--|--|
| Added | `allow_subject_creation` | Boolean | Check if a subject type allows subject creation |
| Added | `is_carrying_or_loaded_unit` | Boolean | Mercenary's underlying unit is embarked on another fleet or has armies embarked on board. Gate destruction/delist actions on this — otherwise the embark link will be torn and the loaded armies will drown. |
