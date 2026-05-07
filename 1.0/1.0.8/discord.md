# Release 1.0.8
## Breaking Changes
Please let me know of any breaking changes you guys discover.
I will add them here.
## Type Documentation
### Disease
- Added `secondary_map_color` documentation
### Scripted Relations
- Changed `offer_visible` documentation (`trigger` instead of `bool`)
- Changed `request_visible` documentation (`trigger` instead of `bool`)
- Changed `cancel_visible` documentation (`trigger` instead of `bool`)
- Changed `break_visible` documentation (`trigger` instead of `bool`)
- Added `show_break_alert` documentation

**Link:** [Type Documentation](./types)
## Script Documentation
### Effects
- Renamed `every_primary_or_accepted_tolerated_culture` to `every_primary_or_accepted_or_tolerated_culture`
- Renamed `ordered_primary_or_accepted_tolerated_culture` to `ordered_primary_or_accepted_or_tolerated_culture`
- Renamed `random_primary_or_accepted_tolerated_culture` to `random_primary_or_accepted_or_tolerated_culture`
### Triggers
- Renamed `any_primary_or_accepted_tolerated_culture` to `any_primary_or_accepted_or_tolerated_culture`
- Added `average_estate_satisfaction` - How high is the average estate satisfaction in the country? The crown estate gets ignored here.
- Added `disease_affects_pops_here` - Checks if a disease is affecting some migrated pops here.
- Added `disease_has_outbreak_here` - Checks if a disease has an outbreak in a location or subunit.
- Added `local_estate_power` - Checks the raw local estate power in location
- Added `local_relative_estate_power` - Checks the relative local estate power in location
- Added `province_population` - Checks if a Province has a certain population
### Modifiers
- Added `shared_border_impact`
- Added `invite_foreign_cleric_cost_modifier`
- Added `local_prosperity_decay`
- Added `global_prosperity_decay`
- Added `union_allowed_enforce_peace`
- Added `unlock_prikazi_reform_cabinet_actions`
### On Actions
- Added `on_country_rank_change`

**Link:** [Script Documentation](./docs)
## Data Type Documentation
Data Type changes can be found below.

**Link:** [Data Type Changes](./changes_data_type.md)
## File Changes
File changes can be found below.

**Link:** [File Changes](./changes_files.md)
## Digest Repository
- https://github.com/Europa-Universalis-5-Modding-Co-op/modding-digests