# Release 1.2.0
## Breaking Changes
- Replaced `location_infection_spread_threshold` disease parameter with `location_spread_threshold`
- Removed `remove_trust` effect
- Removed `reverse_add_trust` effect
- Removed `ai_unlock_unit_score` trigger
- Removed `get_trust` trigger
- Split `army_cavalry_` modifiers into `army_heavy_cavalry_` and `army_light_cavalry_`
- Split `army_infantry_` modifiers into `army_heavy_infantry_` and `army_light_infantry_`
- Replaced `{army\mercenary\merchance\navy}_maintenance_cost` modifiers with `{army\mercenary\merchance\navy}_maintenance_efficiency`
- Replaced `{global\local}_war_score_cost` modifiers with `{global\local}_war_score_efficiency`
- Consolidated `pilgrimage_{religion}_cost_modifier` modifiers into `pilgrimage_action_cost_modifier`
- Split `{disease}_resistance_modifier` modifiers into `local_{disease}_resistance_modifier` and `national_{disease}_resistance_modifier`
- Replaced `trade_{land\sea}_movement_cost_modifier` modifier with `trade_{land\sea}_efficiency`
- Split `trade_efficiency` modifier into `export_efficiency`, `import_efficiency`, and `selling_efficiency`
## Type Documentation
### Area Preferences
- New type
### Building Types
- Added `international_organization_link` to documentation
- Added `international_organization_potential` to documentation
### Bureaucracies
- New type
### Diseases
- Added `potential` to documentation
- Changed `location_infection_spread_threshold` to `location_spread_threshold`
- Added `specific_pop_type_effect` to documentation: Added `culture`, `religion`, `religion_group`, `language`, `language_family` as valid options
- Added `national\local_<tag>_resistance_modifier` to documentation: New modifier types
- Added `national\local_<tag>_growth_modifier` to documentation: New modifier types
### International Organizations
- Added `joins_defensive_wars_as_co_belligerent` to documentation
- Added `joins_offensive_wars_as_co_belligerent` to documentation
- Added `take_over_wars_when_called` to documentation
- Added `has_buildings` to documentation
### Movements
- New Type
### Subject Types
- Added `visible` to documentation
- Added `enabled` to documentation
- Added `on_overlord_becomes_a_subject` to documentation
- Added `counts_as_external` to documentation
### Town Rights
- New Type
### Resolutions
- Added `ai_will_select` to documentation
### Town Rights
- New Type

## Data Type Documentation 
 * [Types](changes_data_types.md#types)
 * [Global Promotes](changes_data_types.md#global-promotes)
## Script Documentation 
 * [Effects](changes_script_docs.md#effects)
 * [Triggers](changes_script_docs.md#triggers)
 * [Event Targets](changes_script_docs.md#event-targets)
 * [Iterators](changes_script_docs.md#iterators)
 * [On Actions](changes_script_docs.md#on-actions)
## File Changes
File changes can be found below.

**Link:** [File Changes](./changes_files.md)
## Digest Repository
- https://github.com/Europa-Universalis-5-Modding-Co-op/modding-digests