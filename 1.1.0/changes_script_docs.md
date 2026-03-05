# Release 1.1.0 - Script Documentation
## Effects
### Variable Maps
| Modififcation Type | Effect                                                | Description                                                    |
|--------------------|-------------------------------------------------------|----------------------------------------------------------------|
| Added              | `add_to_global_variable_map`                          | Adds the event target to a variable map for the given duration |
| Added              | `add_to_local_variable_map`                           | Adds the event target to a variable map for the given duration |
| Added              | `add_to_variable_map`                                 | Adds the event target to a variable map for the given duration |
| Added              | `clear_global_variable_map`                           | Empties the map                                                |
| Added              | `clear_local_variable_map`                            | Empties the map                                                |
| Added              | `clear_variable_map`                                  | Empties the map                                                |
| Added              | `{every\|random\|ordered}_key_in_global_variable_map` | Iterate through all keys in variable map                       |
| Added              | `{every\|random\|ordered}_key_in_local_variable_map`  | Iterate through all keys in variable map                       |
| Added              | `{every\|random\|ordered}_key_in_variable_map`        | Iterate through all keys in variable map                       |
### Scripted Geography
| Modififcation Type | Effect                                                               | Description                                          |
|--------------------|----------------------------------------------------------------------|------------------------------------------------------|
| Added              | `{every\|random\|ordered}_area_in_scripted_geography`                | Iterate through all elements in a scripted geography |
| Added              | `{every\|random\|ordered}_continent_in_scripted_geography`           | Iterate through all elements in a scripted geography |
| Added              | `{every\|random\|ordered}_ownable_location_in_scripted_geography`    | Iterate through all elements in a scripted geography |
| Added              | `{every\|random\|ordered}_location_in_scripted_geography`            | Iterate through all elements in a scripted geography |
| Added              | `{every\|random\|ordered}_province_definition_in_scripted_geography` | Iterate through all elements in a scripted geography |
| Added              | `{every\|random\|ordered}_region_in_scripted_geography`              | Iterate through all elements in a scripted geography |
| Added              | `{every\|random\|ordered}_sub_continent_in_scripted_geography`       | Iterate through all elements in a scripted geography |
| Changed            | `{every\|random\|ordered}_country_with_capital_in_geography`         | Added `scripted_geography` to supported scopes       |
| Changed            | `{every\|random\|ordered}_present_country`                           | Added `scripted_geography` to supported scopes       |
| Changed            | `{every\|random\|ordered}_present_overlord`                          | Added `scripted_geography` to supported scopes       |
### Other
| Modififcation Type | Effect                                                                | Description                                                                                  |
|--------------------|-----------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| Added              | `add_complacency`                                                     | Adds complacency                                                                             |
| Added              | `change_<type>_modifier_size`                                         | Change the strength of a modifier applied to the scope (e.g. `change_country_modifier_size`) |
| Added              | `change_siege_progress`                                               | Advances the siege by the given script value                                                 |
| Added              | `define_unique_country_tag`                                           | defines a unique country tag for a dynamic country                                           |
| Added              | `{every\|random\|ordered}_advance_definition`                         | Iterate through all advance definitions                                                      |
| Added              | `{every\|random\|ordered}_country_with_relation_that_can_be_annulled` | Iterate through all countries which have an annullable relation with the scope country       |
| Added              | `{every\|random\|ordered}_food_goods`                                 | Iterate through all food-goods                                                               |
| Added              | `{every\|random\|ordered}_known_institution`                          | Iterate through all institutions a country knows of                                          |
| Added              | `{every\|random\|ordered}_new_world_goods`                            | Iterate through all newworld-goods                                                           |
| Added              | `{every\|random\|ordered}_old_world_goods`                            | Iterate through all oldworld-goods                                                           |
| Added              | `{every\|random\|ordered}_religious_school_in_religion`               | Iterate through all Religious Schools in a Religion                                          |
| Added              | `{every\|random\|ordered}_sound_toll_in_country`                      | Iterate through all Sound Tolls in a country                                                 |
| Added              | `leave_all_wars_with`                                                 | The current country scope will leave every war with or against the target country            |
| Added              | `set_complacency`                                                     | Sets complacency                                                                             |
| Added              | `transfer_location_occupation`                                        | Transfers occupation of a Location to the target country                                     |
| Added              | `transfer_subject`                                                    | Copy the name and adjective of the target country and apply it to the current country scope  |
| Changed            | `declare_war`                                                         |                                                                                              |
| Changed            | `declare_war_with_cb`                                                 |                                                                                              |
| Changed            | `join_war_against`                                                    | Add `ignore_rules` option                                                                    |
| Changed            | `join_war_as_attacker`                                                | Add `ignore_rules` option                                                                    |
| Changed            | `join_war_as_defender`                                                | Add `ignore_rules` option                                                                    |
| Changed            | `join_war_with`                                                       | Add `ignore_rules` option                                                                    |
| Changed            | `perform_diplomatic_action`                                           |                                                                                              |
| Changed            | `set_new_foreign_ruler_no_update`                                     |                                                                                              |
| Changed            | `set_new_ruler_no_update`                                             |                                                                                              |
| Removed            | `{every\|random\|ordered}_culture_in_group`                           |                                                                                              |
| Removed            | `change_country_tag`                                                  |                                                                                              |
## Triggers
### Variable Maps
| Modififcation Type | Trigger                           | Description                                                     |
|--------------------|-----------------------------------|-----------------------------------------------------------------|
| Added              | `global_variable_map_size`        | Checks the size of a variable map                               |
| Added              | `local_variable_map_size`         | Checks the size of a variable map                               |
| Added              | `variable_map_size`               | Checks the size of a variable map                               |
| Added              | `has_global_variable_map`         | Checks whether the current scope has the specified variable map |
| Added              | `has_local_variable_map`          | Checks whether the current scope has the specified variable map |
| Added              | `has_variable_map`                | Checks whether the current scope has the specified variable map |
| Added              | `is_key_in_global_variable_map`   | Checks if a target is a key in a variable list                  |
| Added              | `is_key_in_local_variable_map`    | Checks if a target is a key in a variable list                  |
| Added              | `is_key_in_variable_map`          | Checks if a target is a key in a variable list                  |
| Added              | `is_value_in_global_variable_map` | Checks if a target is a value in a variable list                |
| Added              | `is_value_in_local_variable_map`  | Checks if a target is a value in a variable list                |
| Added              | `is_value_in_variable_map`        | Checks if a target is a value in a variable list                |
| Added              | `any_key_in_global_variable_map`  | Iterate through all keys in variable map                        |
| Added              | `any_key_in_local_variable_map`   | Iterate through all keys in variable map                        |
| Added              | `any_key_in_variable_map`         | Iterate through all keys in variable map                        |
### Scripted Geography
| Modififcation Type | Trigger                                         | Description                                           |
|--------------------|-------------------------------------------------|-------------------------------------------------------|
| Added              | `is_in_scripted_geography`                      | Checks if the scope is part of the scripted geography |
| Added              | `any_area_in_scripted_geography`                | Iterate through all elements in a scripted geography  |
| Added              | `any_continent_in_scripted_geography`           | Iterate through all elements in a scripted geography  |
| Added              | `any_ownable_location_in_scripted_geography`    | Iterate through all elements in a scripted geography  |
| Added              | `any_location_in_scripted_geography`            | Iterate through all elements in a scripted geography  |
| Added              | `any_province_definition_in_scripted_geography` | Iterate through all elements in a scripted geography  |
| Added              | `any_region_in_scripted_geography`              | Iterate through all elements in a scripted geography  |
| Added              | `any_sub_continent_in_scripted_geography`       | Iterate through all elements in a scripted geography  |
| Changed            | `any_country_with_capital_in_geography`         | Added `scripted_geography` to supported scopes        |
| Changed            | `any_present_country`                           | Added `scripted_geography` to supported scopes        |
| Changed            | `any_present_overlord`                          | Added `scripted_geography` to supported scopes        |
| Changed            | `culture_group_percentage`                      | Added `scripted_geography` to supported scopes        |
| Changed            | `culture_group_population`                      | Added `scripted_geography` to supported scopes        |
| Changed            | `culture_percentage`                            | Added `scripted_geography` to supported scopes        |
| Changed            | `culture_population`                            | Added `scripted_geography` to supported scopes        |
| Changed            | `location_counter`                              | Added `scripted_geography` to supported scopes        |
| Changed            | `population`                                    | Added `scripted_geography` to supported scopes        |
| Changed            | `religion_group_percentage`                     | Added `scripted_geography` to supported scopes        |
| Changed            | `religion_group_population`                     | Added `scripted_geography` to supported scopes        |
| Changed            | `religion_percentage`                           | Added `scripted_geography` to supported scopes        |
| Changed            | `religion_population`                           | Added `scripted_geography` to supported scopes        |
### Other
| Modififcation Type | Trigger                                          | Description                                                                                                                  |
|--------------------|--------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| Added              | `advance_no_longer_activated`                    | Checks if a country has researched a certain advance but it's not useable at the moment because of conditions                |
| Added              | `any_advance_definition`                         | Iterate through all advance definitions                                                                                      |
| Added              | `any_country_with_relation_that_can_be_annulled` | Iterate through all countries which have an annullable relation with the scope country                                       |
| Added              | `any_food_goods`                                 | Iterate through all food-goods                                                                                               |
| Added              | `any_known_institution`                          | Iterate through all institutions a country knows of                                                                          |
| Added              | `any_new_world_goods`                            | Iterate through all newworld-goods                                                                                           |
| Added              | `any_old_world_goods`                            | Iterate through all oldworld-goods                                                                                           |
| Added              | `any_religious_school_in_religion`               | Iterate through all Religious Schools in a Religion                                                                          |
| Added              | `any_sound_toll_in_country`                      | Iterate through all Sound Tolls in a country                                                                                 |
| Added              | `birth_age`                                      | What Age was the character born in? E.g. age_1_traditions                                                                    |
| Added              | `blocks_full_annexation`                         | Checks if the peace treaty blocks full annexation                                                                            |
| Added              | `building_can_be_upgraded_by`                    | Checks if a building can be upgraded by the target country                                                                   |
| Added              | `can_rival`                                      | Could the current country scope rival the target country ignoring slots and range?                                           |
| Added              | `climate_count`                                  | Returns the amount of owned locations with the specified climate.                                                            |
| Added              | `climate_percent`                                | Returns the percentage of owned locations with the specified climate.                                                        |
| Added              | `<type>_modifier_strength`                       | Does the scope have a given modifier with the compared strength (e.g. `country_modifier_strength`)                           |
| Added              | `complacency`                                    | How much complacency does the country/IO have?                                                                               |
| Added              | `complacency_percentage`                         | How high the percentage of the current complacency compared to the maximum does the country/IO have?                         |
| Added              | `days_as_rebel`                                  | Check how many days the character has been a rebel                                                                           |
| Added              | `days_of_service_as_admiral`                     | Check how many days the character has served as an admiral                                                                   |
| Added              | `days_of_service_as_general`                     | Check how many days the character has served as a general                                                                    |
| Added              | `days_of_service_in_cabinet`                     | Check how many days the character has served in a cabinet                                                                    |
| Added              | `favors_needed_to_annul_relations_with`          | Gets the number of favours needed to annul relations with the target country diplomatically                                  |
| Added              | `has_new_world_goods_in_market`                  | Checks if a market has a supply of any new world goods                                                                       |
| Added              | `has_origin_in_new_world`                        | Check if a goods has origin in the new world                                                                                 |
| Added              | `has_origin_in_old_world`                        | Check if a goods has origin in the old world                                                                                 |
| Added              | `has_road_to_capital`                            | Check if a location has a road to capital                                                                                    |
| Added              | `is_a_threat_for_us`                             | Is the country views the target country as a threat?                                                                         |
| Added              | `is_cut_down_in_size_cb`                         | is it a cut down in size CB                                                                                                  |
| Added              | `is_international_organization_annullable`       | Is the international organization able to be annulled by treaty?                                                             |
| Added              | `is_neighbor_of_location_or_across_one_seazone`  | Check if a location is neighbour to another or just across a single seazone                                                  |
| Added              | `is_produced_in_location_market`                 | Checks if a specific goods in produced in the location market                                                                |
| Added              | `is_special_building`                            | Checks if a building is special                                                                                              |
| Added              | `is_subject_type_annullable`                     | Check if a subject type can be annulled by a peace treaty                                                                    |
| Added              | `num_owned_foreign_buildings_in_location`        | The number of foreign buildings in a location owned by a count                                                               |
| Added              | `offer_relation_acceptance`                      | How high is the target country's AI value of accepting the scripted relation offered by the current country scope?           |
| Added              | `owned_by_or_its_subjects`                       | Checks if the geographic scope is completely owned by the target country or its subjects.                                    |
| Added              | `owns_most_foreign_buildings_in_location`        | Does the country own the majority of the foreign buildings in the target location?                                           |
| Added              | `peace_treaty_antagonism`                        | Get how much antagonism the specified peace treaty type would cause for the current country scope against the target country |
| Added              | `peace_treaty_war_score_cost`                    | Get how much war score the specified peace treaty type would cost for the current country scope against the target country   |
| Added              | `policy_level`                                   | Check the defined level of the policy                                                                                        |
| Added              | `request_relation_acceptance`                    | How high is the target country's AI value of accepting the scripted relation requested by the current country scope?         |
| Added              | `reverse_offer_relation_acceptance`              | How high is the current country's AI value of accepting the scripted relation offered by the specified country scope?        |
| Added              | `reverse_request_relation_acceptance`            | How high is the current country's AI value of accepting the scripted relation requested by the specified country scope?      |
| Added              | `subject_type_annullment_favours_required`       | returns the favours needed to annul this relation diplomatically                                                             |
| Added              | `total_foreign_buildings_levels`                 | Checks the total number of foreign buildings of a country                                                                    |
| Added              | `used_fort_limit_percentage`                     | What percentager of our Fort Limit is currently being used?                                                                  |
| Added              | `uses_elections`                                 | Does this succession law use elections?                                                                                      |
| Added              | `years_as_rebel`                                 | Check how many years the character has been a rebel                                                                          |
| Added              | `years_of_service_as_admiral`                    | Check how many years the character has served as an admiral                                                                  |
| Added              | `years_of_service_as_general`                    | Check how many years the character has served as a general                                                                   |
| Added              | `years_of_service_in_cabinet`                    | Check how many years the character has served in a cabinet                                                                   |
| Changed            | `has_doom`                                       | Now only supports `country` scope                                                                                            |
| Changed            | `has_tag`                                        | Added `casus_belli` and `peace_treaty` to supported scopes                                                                   |
| Changed            | `threat_level_to`                                |                                                                                                                              |
| Removed            | `any_culture_in_group`                           |                                                                                                                              |
| Removed            | `unit_has_leader`                                |                                                                                                                              |
## Modifiers
| Modififcation Type | Modifier                                         |
|--------------------|--------------------------------------------------|
| Added              | `ai_require_cb_for_war`                          |
| Added              | `ai_opinion_bias`                                |
| Added              | `global_food_decay`                              |
| Added              | `local_food_decay`                               |
| Added              | `num_bailiffs`                                   |
| Added              | `num_local_governors`                            |
| Added              | `global_peasant_enfranchisment`                  |
| Added              | `local_peasant_enfranchisment`                   |
| Added              | `monthly_complacency`                            |
| Added              | `combined_arms_max_threshold`                    |
| Added              | `combined_arms_min_percent_for_bonus`            |
| Added              | `combined_bonus_per_type`                        |
| Added              | `local_repair_speed`                             |
| Added              | `produced_in_market_bonus`                       |
| Added              | `annexation_speed_base`                          |
| Added              | `annexation_speed_modifier`                      |
| Added              | `enable_doom`                                    |
| Added              | `ignore_doom`                                    |
| Added              | `ai_months_between_wars`                         |
| Added              | `rtr_demand_annexation_price_cost_modifier`      |
| Added              | `complacent_decline_actions_price_cost_modifier` |
| Added              | `unlock_withdraw_from_organization_treasury`     |
| Added              | `enabled_union_enforcement_actions`              |
| Added              | `global_slave_pop_satisfaction`                  |
| Added              | `local_slave_pop_satisfaction`                   |
| Added              | `<terrain>_proximity_impact`                     |
| Added              | `<good>_impacts_inflation`                       |
| Added              | `improve_our_cultural_view_price_cost_modifier`  |
| Added              | `provoke_rebels_price_cost_modifier`             |
| Added              | `transfer_subject_price_cost_modifier`           |
| Removed            | `annexation_speed`                               |
## Event Targets
| Modififcation Type | Event Target                                   | Description                                                                                                                                                        |
|--------------------|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Added              | `original_attacker_leader`                     |                                                                                                                                                                    |
| Added              | `original_defender_leader`                     | Returns the country which was the original defender                                                                                                                |
| Added              | `original_capital`                             |                                                                                                                                                                    |
| Added              | `total_building_levels_including_construction` | The amount of total  building levels including construction in a speficic Country                                                                                  |
| Added              | `advance_age`                                  |                                                                                                                                                                    |
| Added              | `global_variable_map`                          | Reference a previous set variable via its name eg: "global_variable_map(average_relation_map|c:FRA)"                                                               |
| Added              | `local_variable_map`                           | Reference a previous set variable via its name eg: "local_variable_map(rewards_for_country|c:FRA)"                                                                 |
| Added              | `variable_map`                                 | Reference a variable set under a specified scope in a named container on this scope: "variable_map(our_relations_with|c:FRA)"                                      |
| Added              | `scripted_geography`                           |                                                                                                                                                                    |
| Added              | `unit_formation_preference`                    |                                                                                                                                                                    |
| Added              | `war_goal_province`                            | Links to the war goal of the war. If no war goal is set or is unrelated to locations (such as superiority) the link returns the capital of the defender war leader |
## On Actions
| Modififcation Type | On Action                                      | Description                      |
|--------------------|------------------------------------------------|----------------------------------|
| Added              | `on_lose_hegemon_status`                       |                                  |
| Added              | `on_culture_changed`                           |                                  |
| Added              | `on_gain_hegemon_status`                       |                                  |
| Changed            | `on_character_death`                           | The expected scope is now `none` |

**Link:** [Script Documentation](./docs)