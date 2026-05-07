# Release 1.2.0 - Type Documentation
## Area Preferences
- New type
## Building Types
- Added `international_organization_link` (IO type) to documentation
- Added `international_organization_potential` (trigger) to documentation
- Added `capital_to_overlord_modifier` (modifier) to documentation
- Added `foreign_country_modifier` (modifier) to documentation
## Bureaucracies
- New type
## Casus Belli
- Changed  `visible` (trigger) to `create_visible`
- Changed  `allow_creation` (trigger) to `create_enabled`
- Changed  `allow_declaration` (trigger) to `declare_enabled`
- Added `additional_war_enthusiasm` (script value) to documentation: Added `scope:attacker = war leader of the attackers`, `scope:defender = war leader of the defenders`, `scope:target = target character (optional)`, `scope:target_province = target province (optional)`, `scope:target_country = target country (optional)`
- Added `allow_white_peace` (boolean) to documentation
- Added `required_peace_treaties` (peace treaties list) to documentation
- Added `required_attacker_peace_treaties` (peace treaties list) to documentation
- Added `required_defender_peace_treaties` (peace treaties list) to documentation
## Child Educations
- Added `potential` (trigger) to documentation: Added `root` as character scope
- Changed `allow` (trigger) to documentation: Added `root` as character scope
- Added `on_education_start_effect` (effect) to documentation: Added `root` as character scope
## Country Interactions
- Added `source_flags` (flag list) to documentation: Added `wants_military_access_in`
- Added `source_flags_ai_override` (flag list) to documentation: Added `wants_military_access_in`
## Disasters
- Added `custom_description` (localization) to documentation
## Diseases
- Added `potential` (trigger) to documentation
- Changed `location_infection_spread_threshold` (script value) to `location_spread_threshold`
- Added `specific_pop_type_effect` (special) to documentation: Added `culture`, `religion`, `religion_group`, `language`, `language_family` as valid options
- Added `local_<tag>_resistance_modifier` (modifier type) to documentation: New modifier type
- Added `national_<tag>_resistance_modifier` (modifier type) to documentation: New modifier type
- Added `local_<tag>_growth_modifier` (modifier type) to documentation: New modifier type
- Added `national_<tag>_growth_modifier` (modifier type) to documentation: New modifier type
## Formable Countries
- Added `potential_requires_own` (boolean) to documentation
## Gods
- Added `is_female` (boolean) to documentation
## International Organizations
- Added `joins_defensive_wars_as_co_belligerent` (boolean) to documentation
- Added `joins_offensive_wars_as_co_belligerent` (boolean) to documentation
- Added `take_over_wars_when_called` (boolean) to documentation
- Added `has_buildings` (boolean) to documentation
## Movements
- New Type
## Resolutions
- Added `show_target_in_tooltip` (boolean) to documentation
## Road Types
- Added `pop_movement` (number) to documentation
## Resolutions
- Added `move_to_next_section_on_click` (boolean) to documentation
## Situations
- Added `custom_description` (localization) to documentation
## Subject Types
- Added `visible` (trigger) to documentation
- Added `enabled` (trigger) to documentation
- Added `on_overlord_becomes_a_subject` (flag) to documentation
- Added `counts_as_external` (boolean) to documentation
## Town Rights
- New Type
## Unit Categories
- Added `fallback` (unit_category_id) to documentation
## Unit Types
- Removed `light` (boolean) from documentation
## Wargoals
- Added `release_cost` (float) to documentation

**Link:** [Type Documentation](./types)