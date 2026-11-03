# Script Documentation 1.4.7
## Notes
 * **Changed** means the description, scopes or anything related to the documentation for this element has changed
 * The list of iterators do **not** include generated geographic region based iterators
 * The on action scope is based on the script documentation, for more information see the `common/on_actions` directory

## Triggers
| Type | Trigger | Trait | Description |
|--|--|--|--|
| Added | `tariffs_paid_to` | Value | gold the scope country's trades paid in tariffs last month to markets owned by the target. tariffs_paid_to = { target = X \[*value \>/\</\>=/\<= Y* or *value = { min max }*  } |
