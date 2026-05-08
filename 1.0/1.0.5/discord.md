# Release 1.0.5
## Breaking Changes
Please let me know of any breaking changes you guys discover.
I will add them here.
## Official Patch Notes
- Can use `[COUNTRY.GetDominantLanguage]` to get the Dominant Language of a Country in the Loc script
- Can now scope from Pop to its Dialect
- Added the `wants_keep_policy` and `reasons_to_join` script value traits for policies
- Expanded the `rebel_category` trigger to now work on the country scope, too. Rebel countries will this way now have a way to recall which rebel category they have been spawned from
- The `international_organization_num_locations` trigger now shows the current value of locations the IO owns
- The `international_organization_population` trigger now shows the current value in the correct population format.
- Fixed a localization issue of the `culture_opinion_impact`, which prevented the target culture from being shown
- Added the `ai_policy_resolution_keep_bias`, `ai_policy_reason_to_join`, `policy_has_ai_vote_value`, `policy_has_ai_keep_value` and `policy_has_ai_join_reason` triggers for policies
- Updated the `resolution_opinion` to properly work in an conventional writing style (`resolution_opinion = { international_organization = <international organization> resolution = <resolution> vote = <vote scope> value = <value> }`) and fixed the lack of tooltipping for it
## Script Documentation
### Effects
- Added `update_leadership`
### Triggers
- Added `ai_policy_reason_to_join`
- Added `ai_policy_resolution_keep_bias`
- Added `food_maintenance`
- Added `is_foreign`
- Added `is_owned_by_country`
- Added `policy_has_ai_join_reason`
- Added `policy_has_ai_keep_value`
- Added `policy_has_ai_vote_value`
- Added `relative_defensive_alliance_strength`
### Event Targets
- Added `name_culture`
### On Actions
- Added `on_character_estate_change`

**Link:** [Documentation](./docs)
## File Changes
File changes can be found below.

**Link:** [File Changes](./changes_files.md)
## Digest Repository
- https://github.com/Europa-Universalis-5-Modding-Co-op/modding-digests