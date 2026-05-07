# Release 1.0.10 - Script Documentation
## Effects
- Added `add_dynasty_modifier` - Add a modifier to a dynasty
- Added `annul_all_treaties_with` - The current country scope annuls all treaties with the target country
- Added `change_location_owner_forcefully` - Change owner of Location to target country but forcefully
- Added `destroy_building_forcefully` - Destroys the specified building in the location
- Added `remove_all_casus_belli_of_type` - Removes the casus belli of the specified type against ALL other countries
- Added `remove_dynasty_modifier` - Remove a modifier from a dynasty
- Changed `add_casus_belli` documentation
- Changed `declare_war_with_cb` documentation
- Changed `destroy_building` documentation
- Changed `remove_relation` documentation
- Removed `{ordered|random|every}_country_with_antagonism_against_us`
## Triggers
- Added `annexation_progress` - How high is the annexation progress of the target country for the current country scope?
- Added `bias_value` - Get the value of the given bias modifier
- Added `building_can_be_destroyed_by` - Check if the target country scope is capable of destroying the current building scope
- Added `has_casus_belli_of_type` - Does the country have a cb of the specified type against any country?
- Added `has_dynasty_modifier` - Does the scoped dynasty have a given modifier
- Added `has_rebel_modifier` - Does the scoped rebel have a given modifier
- Added `is_eligible_for_royal_marriage` - If character is eligible for royal marriage
- Added `is_leading_largest_army_of` - The character is leading the largest land unit of the target country
- Added `is_leading_largest_navy_of` - The character is leading the largest navy unit of the target country
- Added `num_cabinet_capable_characters` - Checks if a country has a certain amount of characters who can do cabinet
- Added `num_explorations_including_in_construction` - Checks if a country has a certain amount of Explorations including those under construction
- Added `province_pop_type_population` - Check how much goods the scope location produces
- Added `religious_view_impact` - Opinion impact of a particular religion on another
- Added `unfilled_jobs_in_province` - Gets the number of unfilled jobs in the province
- Added `unfilled_jobs_in_province_percentage` - Gets the percentage of unfilled jobs in the province
- Added `wants_to_attack` - Country wants to attack another country?
- Removed `has_countries_with_antagonism`
## Modifiers
- Added `force_convert_created_subjects`
- Added `hostile_diplomatic_annexation_cost`
- Added `force_army_maintenance`
- Added `local_market_access`
- Added `block_tribal_promotion`
- Added `levy_recovery_modifier`
- Added `union_blocked_from_declaring_war`
- Added `{disease}_resistance_modifier`
- Added `union_unlock_rein_in_junior_diplomacy`
- Added `cannot_be_subjugated`
## Event Targets
- Added `largest_army`
- Added `largest_navy`
- Removed `source_province`
## On Actions
- Added `on_subject_created`

**Link:** [Script Documentation](./docs)