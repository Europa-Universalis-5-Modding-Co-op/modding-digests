# Script Documentation 1.2.0
## Table of Contents
* [Effects](#effects)
* [Triggers](#triggers)
* [Event Targets](#event-targets)
* [Iterators](#iterators)
* [On Actions](#on-actions)
## Notes
* **Changed** means the description, scopes or anything related to the documentation for this element has changed
* The on action scope is based on the script documentation, for more information see the `common/on_actions` directory

## Effects
| Type    | Effect                                       | Description                                                                                                          |
| ------- | -------------------------------------------- | -------------------------------------------------------------------------------------------------------------------- |
| Added   | `add_area_preference`                        | Adds an area preference to the AI of a country                                                                       |
| Added   | `add_bureaucracy`                            | Adds a new bureaucracy of the supplied type to the country's government.                                             |
| Added   | `add_movement_modifier`                      | add a modifier to a movement                                                                                         |
| Added   | `add_omen`                                   | adds an omen to a country                                                                                            |
| Added   | `add_omen_god`                               | adds god to a country to ask for guidance on selecting an omen                                                       |
| Added   | `add_spreader`                               | Adds a character who is spreading the movement.                                                                      |
| Added   | `add_trust_equilibrium`                      | Adds a trust equilibrium modifier,                                                                                   |
| Added   | `change_entrenchment`                        | Modifies the entrenchment of a bureaucracy by however much                                                           |
| Added   | `change_score`                               | gives (or takes) score a country                                                                                     |
| Added   | `demote_accepted_culture`                    | Removes an accepted culture and adds it as tolerated, with a single pop status update                                |
| Added   | `destroy_building_country`                   | destroys building based country removing all their buildings and releasing subjects.                                 |
| Added   | `distribute_gold_to_banking_estates`         | Distributes gold proportionally to all banking estates in a country                                                  |
| Added   | `grant_town_rights`                          | grant town rights to a location                                                                                      |
| Added   | `io_recalculate_leader`                      | force an international organization to recalculate its character leader from the current ruler of the leader country |
| Added   | `lock_maintenance`                           | Sets the maintenance of a bureaucracy to be locked or not                                                            |
| Added   | `marry_character_ignore_blocks`              | Marries character to target character, ignoring social restrictions such as estate, modifiers and same sex ban       |
| Added   | `remove_all_area_preferences`                | Removes all area preferences from the AI of a country                                                                |
| Added   | `remove_area_preference`                     | Removes an area preference from the AI of a country                                                                  |
| Added   | `remove_bureaucracy`                         | removes the supplied bureaucracy from the country's government.                                                      |
| Added   | `remove_movement_modifier`                   | Remove a modifier from a movement                                                                                    |
| Added   | `remove_omen`                                | removes an omen from a country                                                                                       |
| Added   | `remove_spreader`                            | Stops a character from spreading the movement.                                                                       |
| Added   | `remove_trust_equilibrium`                   | Removes a trust equilibrium modifier,                                                                                |
| Added   | `reset_ruler_title`                          | resets a ruler's title so it gets generated again                                                                    |
| Added   | `reverse_add_trust_equilibrium`              | Adds a reverse trust equilibrium modifier,                                                                           |
| Added   | `revoke_town_rights`                         | Revoke a specific town rights                                                                                        |
| Added   | `revoke_town_rights_of_type`                 | revoke town rights of a type from a location                                                                         |
| Added   | `set_entrenchment`                           | Sets the entrenchment of a bureaucracy to the supplied value                                                         |
| Added   | `set_maintenance`                            | Sets the maintenance of a bureaucracy to the supplied value                                                          |
| Added   | `set_personality`                            | Sets the AI personality for a country                                                                                |
| Added   | `spawn_movement`                             | Spawns a movement in a location or on a subunit.                                                                     |
| Added   | `spread_to_location`                         | Spreads the movement to a new location.                                                                              |
| Changed | `add_trust`                                  | Adds trust (target = x value = y}                                                                                    |
| Changed | `join_war_against`                           | joins the target war as an enemy of the target country.                                                              |
| Changed | `join_war_with`                              | joins the target war as an ally of the target country.                                                               |
| Changed | `remove_character_modifier`                  | Remove a modifier from a character                                                                                   |
| Changed | `remove_country_modifier`                    | Remove a modifier from a country                                                                                     |
| Changed | `remove_dynasty_modifier`                    | Remove a modifier from a dynasty                                                                                     |
| Changed | `remove_god`                                 | removes a god from a country                                                                                         |
| Changed | `remove_international_organization_modifier` | Remove a modifier from an international organization                                                                 |
| Changed | `remove_location_modifier`                   | Remove a modifier from a location                                                                                    |
| Changed | `remove_mercenary_modifier`                  | Remove a modifier from a mercenary                                                                                   |
| Changed | `remove_province_modifier`                   | Remove a modifier from a province                                                                                    |
| Changed | `remove_rebel_modifier`                      | Remove a modifier from a rebel                                                                                       |
| Changed | `remove_religion_modifier`                   | Remove a modifier from a religion                                                                                    |
| Changed | `remove_unit_modifier`                       | Remove a modifier from a unit                                                                                        |
| Changed | `start_weather_system`                       | Starts off a new weather system.                                                                                     |
| Removed | `remove_trust`                               | Removes a trust modifier,                                                                                            |
| Removed | `reverse_add_trust`                          | Adds a reverse trust modifier,                                                                                       |

## Triggers
| Type    | Trigger                                              | Description                                                                                                                                      | Trait   |
| ------- | ---------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------ | ------- |
| Added   | `allowed_bureaucracies`                              | Check if the country is allowed bureaucracies                                                                                                    | Boolean |
| Added   | `bureaucracy_disliked_by_estate`                     | is this bureaucracy disliked by this estate?                                                                                                     | -       |
| Added   | `bureaucracy_disliked_by_estate_type`                | is this bureaucracy disliked by this estate type?                                                                                                | -       |
| Added   | `bureaucracy_liked_by_estate`                        | is this bureaucracy liked by this estate?                                                                                                        | -       |
| Added   | `bureaucracy_liked_by_estate_type`                   | is this bureaucracy liked by this estate type?                                                                                                   | -       |
| Added   | `bureaucracy_maintenance`                            | current maintenance of the bureaucracy 0-1                                                                                                       | Value   |
| Added   | `bureaucracy_type_disliked_by_estate`                | is this bureaucracy type disliked by this estate?                                                                                                | -       |
| Added   | `bureaucracy_type_disliked_by_estate_type`           | is this bureaucracy type disliked by this estate type?                                                                                           | -       |
| Added   | `bureaucracy_type_is_enabled`                        | Can we use a bureaucracy for a country?                                                                                                          | -       |
| Added   | `bureaucracy_type_is_visible`                        | Can we see a bureaucracy for a country?                                                                                                          | -       |
| Added   | `bureaucracy_type_liked_by_estate`                   | is this bureaucracy type liked by this estate?                                                                                                   | -       |
| Added   | `bureaucracy_type_liked_by_estate_type`              | is this bureaucracy type liked by this estate type?                                                                                              | -       |
| Added   | `can_marry_character`                                | Check if the current character scope can marry the target character                                                                              | -       |
| Added   | `capital_wealth`                                     | Checks the total capital wealth of a country                                                                                                     | Value   |
| Added   | `colonial_charter_distance`                          | Straight-line distance from country capital to a province's first passable location. Cheap sort proxy for colonial_charter_utility.)             | Value   |
| Added   | `conquer_area_preference`                            | Gets the AI conquer preference for the supplied area -                                                                                           | Value   |
| Added   | `entrenchment`                                       | current entrenchment of the bureaucracy 0-100                                                                                                    | Value   |
| Added   | `get_trust_equilibrium`                              | how much of a trust equilibrium type does the country have towards another country?                                                              | Value   |
| Added   | `gives_defensive_support_to`                         | Does the scope country give defensive support to specified country?                                                                              | -       |
| Added   | `gives_offensive_support_to`                         | Does the scope country give offensive support to specified country?                                                                              | -       |
| Added   | `had_country_rank_level`                             | Checks if a country has been or is currently in that level of the country rank                                                                   | -       |
| Added   | `harbor_capacity_in_area`                            | gets the sum of harbor capacity (harbor suitability) at the country's ports in an area                                                           | Value   |
| Added   | `has_ai_disposition_toward_player`                   | Does the country view the player with the given AI disposition? (alarmed/wary/planning_war/covets/rivals/indifferent)                            | -       |
| Added   | `has_ai_preferred_parliament_law_change`             | Checks if the AI has a preferred parliament law change stored                                                                                    | Boolean |
| Added   | `has_any_rgo_of_goods_method`                        | True if the country owns at least one location whose raw material uses the specified goods method.                                               | -       |
| Added   | `has_any_town_rights`                                | Check if a location has town rights                                                                                                              | Boolean |
| Added   | `has_area_preference`                                | Checks if a country has a specific area preference active                                                                                        | -       |
| Added   | `has_bureaucracy_of_type`                            | checks if the scope country has a bureaucracy of the supplied type                                                                               | -       |
| Added   | `has_different_town_rights_than`                     | Checks if a location shares no town right types with another location                                                                            | -       |
| Added   | `has_max_town_rights`                                | Check if a location has reached its maximum number of town rights                                                                                | Boolean |
| Added   | `has_old_world_goods_in_market`                      | Checks if a market has a supply of any old world goods                                                                                           | Boolean |
| Added   | `has_omens`                                          | religion has omens                                                                                                                               | Boolean |
| Added   | `has_only_prisoners`                                 | returns true if the unit contains ONLY prisoners                                                                                                 | Boolean |
| Added   | `has_personality`                                    | Does the country have the specified AI personality?                                                                                              | -       |
| Added   | `has_preference_tag`                                 | if a country has specific preference tag                                                                                                         | -       |
| Added   | `has_town_rights`                                    | Checks if a location has a specific town_rights                                                                                                  | -       |
| Added   | `importance`                                         | Checks if a Holy Site has this Importance                                                                                                        | Value   |
| Added   | `international_organization_economical_base`         | Checks if an international organization has a certain economical base based on their members                                                     | Value   |
| Added   | `io_exists`                                          | Does the international organization exist?                                                                                                       | -       |
| Added   | `io_total_great_power_score`                         | returns the cached sum of great power scores of all members of an international organization (updated monthly)                                   | Value   |
| Added   | `io_total_military_strength`                         | returns the cached sum of army strengths of all members of an international organization (updated monthly)                                       | Value   |
| Added   | `is_active`                                          | If a culture is active.                                                                                                                          | Boolean |
| Added   | `is_ai_preferred_parliament_change_law`              | Checks if this law is the AI's preferred parliament law change target (pass actor country as argument)                                           | -       |
| Added   | `is_ai_preferred_parliament_change_policy`           | Checks if this policy is the AI's preferred parliament policy change target (pass actor country as argument)                                     | -       |
| Added   | `is_eligible_for_marriage`                           | Check if the current character scope can marry                                                                                                   | Boolean |
| Added   | `is_god_female`                                      | is the god female?                                                                                                                               | Boolean |
| Added   | `is_invoking_omen`                                   | country is invoking omen                                                                                                                         | Boolean |
| Added   | `is_location_holy_site_type`                         | Is the location a holy site of the specified type?                                                                                               | -       |
| Added   | `is_selected_omen_god`                               | If a god is the one asked for guidance for selecting an omen in the target country                                                               | -       |
| Added   | `language_population_in_country`                     | The number of speakers of a specific language in the current country                                                                             | Value   |
| Added   | `max_bureaucracy_slots`                              | Checks if a country has a certain amount of maximum bureaucracy slots                                                                            | Value   |
| Added   | `merged_culture_group_contains_culture`              | True if this merged culture was formed from a culture group that contained the target culture.                                                   | -       |
| Added   | `monarch_power_percentage_in_country`                | The percentage of a specific monarch power in the current country                                                                                | Value   |
| Added   | `monthly_population_change`                          | Check how much the population changes on a monthly base based on the previous month's data                                                       | Value   |
| Added   | `monthly_satisfaction_change`                        | The monthly satisfaction change of an estate                                                                                                     | Value   |
| Added   | `movement_presence`                                  | Checks the number of pops affected by a movement in a location or subunit.                                                                       | Value   |
| Added   | `num_adult_available_dynasty_members`                | Return the number of living adult dynasty members who are neither rulers nor heirs                                                               | Value   |
| Added   | `num_buildings_owned_by_estate`                      | Checks how many buildings an estate has                                                                                                          | Value   |
| Added   | `num_bureaucracies`                                  | Checks if a country has a certain amount of bureaucracies active                                                                                 | Value   |
| Added   | `num_country_that_can_be_called_offensively`         | Checks the number of countries that can be called into an offensive war by this country                                                          | Value   |
| Added   | `num_locations_affected`                             | calculates the number of locations affected by the movement.                                                                                     | Value   |
| Added   | `num_of_common_rivals`                               | calculates the amount of common rivals between two countries.                                                                                    | Value   |
| Added   | `num_of_common_rivals_and_enemies`                   | calculates the amount of common rivals and enemies between two countries.                                                                        | Value   |
| Added   | `num_omens`                                          | Checks if a country has a certain amount of omens                                                                                                | Value   |
| Added   | `num_open_bureaucracy_slots`                         | Checks if a country has a certain amount of open bureaucracy slots                                                                               | Value   |
| Added   | `original_location_rank`                             | Check if a location's rank at campaign start matches the supplied location rank                                                                  | -       |
| Added   | `original_tag`                                       | if a country is a specific historical tag or was it.                                                                                             | -       |
| Added   | `owns_or_non_sovereign_subject_owns_entire_province` | Does the country or non-sovereign subjects own all locations in province?                                                                        | -       |
| Added   | `policy_possible_for_country`                        | Check the is a policy is possible for target counntry                                                                                            | -       |
| Added   | `policy_utility`                                     | Utility of a policy that can subtract the utility of current policy -                                                                            | Value   |
| Added   | `prev_favors_with_this`                              | Gets the previous scope country's favors with the current scope country                                                                          | Value   |
| Added   | `prev_spy_network_in_this`                           | Gets the previous scope country's spy network in the current scope country                                                                       | Value   |
| Added   | `prev_trust_equilibrium_of_this`                     | Gets the previous scope country's trust equilibrium of the current scope country                                                                 | Value   |
| Added   | `province_location_wealth`                           | Checks if a Province has a certain total location wealth (possible tax base)                                                                     | Value   |
| Added   | `receives_defensive_support_from`                    | Does the scope country receive defensive support from the specified country?                                                                     | -       |
| Added   | `receives_offensive_support_from`                    | Does the scope country receive offensive support from the specified country?                                                                     | -       |
| Added   | `religion_group_population_in_country`               | The number of population a specific religion group in the current country                                                                        | Value   |
| Added   | `rgo_level`                                          | Checks if a location has a certain rgo level                                                                                                     | Value   |
| Added   | `this_favors_with_prev`                              | Gets the current scope country's favors with the previous scope country                                                                          | Value   |
| Added   | `this_spy_network_in_prev`                           | Gets the current scope country's spy network in the previous scope country                                                                       | Value   |
| Added   | `this_trust_equilibrium_of_prev`                     | Gets the current scope country's trust equilibrium of the previous scope country                                                                 | Value   |
| Added   | `trust_equilibrium`                                  | is the country's trust equilibrium towards the target greater or equal than the value?                                                           | Value   |
| Added   | `unemployed_pops_of_pop_type_in_location`            | gets the number of unemployed pops of the pop type in the location                                                                               | Value   |
| Added   | `unemployed_pops_of_pop_type_in_province`            | gets the number of unemployed pops of the pop type in the province                                                                               | Value   |
| Added   | `valid_gender_for_heir_selection`                    | Checks if the character's gender is allowed for the target heir selection                                                                        | -       |
| Changed | `culture_group_population_in_country`                | The number of population of a specific culture group in the current country                                                                      | Value   |
| Changed | `culture_population_in_country`                      | The number of population of a specific culture in the current country                                                                            | Value   |
| Changed | `has_dlc`                                            | Does the host have this DLC enabled? used for synched content                                                                                    | -       |
| Changed | `has_local_dlc`                                      | Does the local player have this DLC enabled? used for unsynched content like new graphics                                                        | -       |
| Changed | `has_prisoners`                                      | returns true if the unit contains prisoners                                                                                                      | Boolean |
| Changed | `has_tag`                                            | Check if that object has the specified tag.                                                                                                      | -       |
| Changed | `implementation_progress_percentage`                 | Checks if the current implementable scope has been implemented in percentage.                                                                    | Value   |
| Changed | `is_allowed_for`                                     | Returns true if the current database object is allowed (but not necessarily visible) for the target country.                                     | -       |
| Changed | `is_available_for`                                   | Returns true if the current database object is available to the target country.                                                                  | -       |
| Changed | `is_eligible_for_royal_marriage`                     | if character is eligible for royal marriage. Is more restrictive and focused on rulers / heirs than the can_marry trigger                        | Boolean |
| Changed | `is_fully_implemented_in`                            | Checks if the current implementable scope has been fully implemented in the specified country                                                    | -       |
| Changed | `is_implementable_in`                                | Checks if the current implementable scope can be implemented in the specified country. Does not check if it has already been implemented or not. | -       |
| Changed | `is_real_country`                                    | Checks if a country is a real country as opposed to mercenaries or pirates                                                                       | Boolean |
| Changed | `is_visible_for`                                     | Returns true if the current database object is visible (but not necessarily allowed) to the target country.                                      | -       |
| Changed | `modifier_utility`                                   | Checks the AI utility of a modifier                                                                                                              | Value   |
| Changed | `modifier_utility_include_locations`                 | Checks the AI utility of a modifier with location checks                                                                                         | Value   |
| Changed | `owns_or_has_subject_in`                             | country directly owns or has a subject in the geography supplied?                                                                                | -       |
| Changed | `pop_type_percentage_in_country`                     | The percentage of population with the specific pop type in the current country                                                                   | Value   |
| Changed | `pop_type_population_in_country`                     | The number of population with the specific pop type in the current country                                                                       | Value   |
| Changed | `province_pop_type_population`                       | Checks how much of a pop type lives in the scope location.                                                                                       | Value   |
| Changed | `religion_population_in_country`                     | The number of population with a specific religion in the current country                                                                         | Value   |
| Changed | `ruled_country_on_or_after`                          | Check if the character has ruled the target country on or after the specified date.                                                              | -       |
| Changed | `trust`                                              | How much trust does the country have in the target?                                                                                              | Value   |
| Removed | `ai_unlock_unit_score`                               | Returns the score for AI to unlock a unit                                                                                                        | Value   |
| Removed | `get_trust`                                          | how much of a trust type does the country have towards another country?                                                                          | Value   |

## Event Targets
| Type  | Event Target                                       | Description                                 |
| ----- | -------------------------------------------------- | ------------------------------------------- |
| Added | `ai_personality`                                   | Unknown, add something in code registration |
| Added | `bureaucracy_type`                                 | Unknown, add something in code registration |
| Added | `movement_definition`                              | Unknown, add something in code registration |
| Added | `omen`                                             | Unknown, add something in code registration |
| Added | `town_rights_type`                                 | Unknown, add something in code registration |
| Added | `ai_personality`                                   | Unknown, add something in code registration |
| Added | `country_government_reform_fully_implemented_date` | Unknown, add something in code registration |
| Added | `country_government_reform_implementation_date`    | Unknown, add something in code registration |
| Added | `implementation_price`                             | Unknown, add something in code registration |
| Added | `removal_price`                                    | Unknown, add something in code registration |
| Added | `movement_type`                                    | Unknown, add something in code registration |
| Added | `linked_pop`                                       | Unknown, add something in code registration |
| Added | `town_rights_type`                                 | Unknown, add something in code registration |
| Added | `bureaucracy_type`                                 | Unknown, add something in code registration | 

## Iterators
| Type  | Iterator                                                           | 
| ----- | ------------------------------------------------------------------ | 
| Added | `{any\every\ordered\random}_available_dynasty_member`              | 
| Added | `{any\every\ordered\random}_building_owned_by_estate`              | 
| Added | `{any\every\ordered\random}_current_bureaucracy`                   | 
| Added | `{any\every\ordered\random}_current_bureaucracy_type`              | 
| Added | `{any\every\ordered\random}_estate_type_that_dislikes_bureaucracy` | 
| Added | `{any\every\ordered\random}_estate_type_that_likes_bureaucracy`    | 
| Added | `{any\every\ordered\random}_location_with_movement`                | 
| Added | `{any\every\ordered\random}_locations_with_town_rights_in_country` | 
| Added | `{any\every\ordered\random}_movement`                              | 
| Added | `{any\every\ordered\random}_movement_in_country`                   | 
| Added | `{any\every\ordered\random}_movement_in_culture`                   | 
| Added | `{any\every\ordered\random}_movement_in_religion`                  | 
| Added | `{any\every\ordered\random}_omen_in_country`                       | 
| Added | `{any\every\ordered\random}_omen_in_god`                           | 
| Added | `{any\every\ordered\random}_omen_in_religion`                      | 
| Added | `{any\every\ordered\random}_ruled_international_organization`      | 
| Added | `{any\every\ordered\random}_town_rights_in_country`                | 
| Added | `{any\every\ordered\random}_town_rights_in_location`               | 
| Added | `{any\every\ordered\random}_trait`                                 | 
## On Actions
| Type  | On Action                   | Scope     | 
| ----- | --------------------------- | --------- | 
| Added | `on_colonize_annexed`       | `none`    | 
| Added | `on_enforce_peace_declined` | `none`    | 
| Added | `on_truce_broken`           | `none`    | 
| Added | `on_bureaucracy_added`      | `none`    | 
| Added | `on_enforce_peace_accepted` | `none`    | 
| Added | `on_parliament_established` | `none`    | 
| Added | `on_shattered_country`      | `none`    | 
| Added | `on_omen_god_selected`      | `country` | 
| Added | `on_parliament_abolished`   | `none`    | 
| Added | `on_bureaucracy_change`     | `none`    | 
| Added | `on_colonize_annex`         | `none`    | 
| Added | `on_bureaucracy_removed`    | `none`    | 
| Added | `on_transfer_subject`       | `none`    | 

## Modifiers
| Modififcation Type | Modifier                                                   | Description |
| ------------------ | ---------------------------------------------------------- | ----------- |
| Removed            | `antagonism_tolerance`                                     |             |
| Removed            | `army_cavalry_build_cost_modifier`                         |             |
| Removed            | `army_cavalry_maintenance_cost_modifier`                   |             |
| Removed            | `army_cavalry_power`                                       |             |
| Removed            | `army_cavalry_reinforce_cost_modifier`                     |             |
| Removed            | `army_infantry_build_cost_modifier`                        |             |
| Removed            | `army_infantry_maintenance_cost_modifier`                  |             |
| Removed            | `army_infantry_power`                                      |             |
| Removed            | `army_infantry_reinforce_cost_modifier`                    |             |
| Removed            | `army_maintenance_cost`                                    |             |
| Removed            | `bubonic_plague_resistance_modifier`                       |             |
| Removed            | `court_spending_cost`                                      |             |
| Removed            | `global_pop_silver_demand`                                 |             |
| Removed            | `global_war_score_cost`                                    |             |
| Removed            | `great_pestilence_resistance_modifier`                     |             |
| Removed            | `influenza_resistance_modifier`                            |             |
| Removed            | `local_war_score_cost`                                     |             |
| Removed            | `malaria_resistance_modifier`                              |             |
| Removed            | `measles_resistance_modifier`                              |             |
| Removed            | `mercenary_maintenance_cost`                               |             |
| Removed            | `merchant_maintenance_cost`                                |             |
| Removed            | `navy_maintenance_cost`                                    |             |
| Removed            | `pilgrimage_jain_cost_modifier`                            |             |
| Removed            | `pilgrimage_piety_cost_modifier`                           |             |
| Removed            | `pilgrimage_purity_cost_modifier`                          |             |
| Removed            | `pilgrimage_yanantin_cost_modifier`                        |             |
| Removed            | `produced_in_market_bonus`                                 |             |
| Removed            | `smallpox_resistance_modifier`                             |             |
| Removed            | `trade_efficiency`                                         |             |
| Removed            | `trade_land_movement_cost_modifier`                        |             |
| Removed            | `trade_sea_movement_cost_modifier`                         |             |
| Removed            | `typhus_resistance_modifier`                               |             |
| Added              | `allelengyon_bureaucracy_impact_modifier`                  |             |
| Added              | `allow_bureaucracy`                                        |             |
| Added              | `allow_roman_movement`                                     |             |
| Added              | `aqueduct_system_max_level`                                |             |
| Added              | `army_heavy_cavalry_build_cost_modifier`                   |             |
| Added              | `army_heavy_cavalry_maintenance_cost_modifier`             |             |
| Added              | `army_heavy_cavalry_power`                                 |             |
| Added              | `army_heavy_cavalry_reinforce_cost_modifier`               |             |
| Added              | `army_heavy_infantry_build_cost_modifier`                  |             |
| Added              | `army_heavy_infantry_maintenance_cost_modifier`            |             |
| Added              | `army_heavy_infantry_power`                                |             |
| Added              | `army_heavy_infantry_reinforce_cost_modifier`              |             |
| Added              | `army_light_cavalry_build_cost_modifier`                   |             |
| Added              | `army_light_cavalry_maintenance_cost_modifier`             |             |
| Added              | `army_light_cavalry_power`                                 |             |
| Added              | `army_light_cavalry_reinforce_cost_modifier`               |             |
| Added              | `army_light_infantry_build_cost_modifier`                  |             |
| Added              | `army_light_infantry_maintenance_cost_modifier`            |             |
| Added              | `army_light_infantry_power`                                |             |
| Added              | `army_light_infantry_reinforce_cost_modifier`              |             |
| Added              | `army_maintenance_efficiency`                              |             |
| Added              | `assign_despot_price_cost_modifier`                        |             |
| Added              | `blind_character_price_cost_modifier`                      |             |
| Added              | `build_hippodrome_price_cost_modifier`                     |             |
| Added              | `byz_born_in_the_purple`                                   |             |
| Added              | `cabinet_trait_impact_modifier`                            |             |
| Added              | `can_grant_town_rights`                                    |             |
| Added              | `can_host_olympiads`                                       |             |
| Added              | `can_ignore_papal_bulls`                                   |             |
| Added              | `capital_possible_town_rights`                             |             |
| Added              | `castrate_character_price_cost_modifier`                   |             |
| Added              | `coalition_strength_tolerance`                             |             |
| Added              | `commander_combat_bonus`                                   |             |
| Added              | `compose_strategikon_price_cost_modifier`                  |             |
| Added              | `contact_patriarch_of_constantinople_cost_modifier`        |             |
| Added              | `country_allow_canonization`                               |             |
| Added              | `country_marriage_banned`                                  |             |
| Added              | `court_eunuchs_bureaucracy_impact_modifier`                |             |
| Added              | `court_spending_cost_modifier`                             |             |
| Added              | `crown_power_from_population`                              |             |
| Added              | `deselect_orthodox_education_cost_modifier`                |             |
| Added              | `enable_pronoia_subject`                                   |             |
| Added              | `expand_aqueduct_system_cost_modifier`                     |             |
| Added              | `expensive_estate_building_cost_modifier`                  |             |
| Added              | `export_efficiency`                                        |             |
| Added              | `export_impact_on_demand`                                  |             |
| Added              | `fate_of_phoenix_actions_price_cost_modifier`              |             |
| Added              | `frankokratia_vassal_state_may_declare_war`                |             |
| Added              | `global_alum_pop_demand`                                   |             |
| Added              | `global_amber_pop_demand`                                  |             |
| Added              | `global_beer_pop_demand`                                   |             |
| Added              | `global_beeswax_pop_demand`                                |             |
| Added              | `global_books_pop_demand`                                  |             |
| Added              | `global_bureaucracy_entrenchment_speed_modifier`           |             |
| Added              | `global_bureaucracy_implementation_cost_modifier`          |             |
| Added              | `global_bureaucracy_maintenance_cost_modifier`             |             |
| Added              | `global_bureaucracy_removal_cost_modifier`                 |             |
| Added              | `global_burghers_pop_growth`                               |             |
| Added              | `global_cannons_pop_demand`                                |             |
| Added              | `global_chili_pop_demand`                                  |             |
| Added              | `global_clay_pop_demand`                                   |             |
| Added              | `global_clergy_pop_growth`                                 |             |
| Added              | `global_cloth_pop_demand`                                  |             |
| Added              | `global_cloves_pop_demand`                                 |             |
| Added              | `global_coal_pop_demand`                                   |             |
| Added              | `global_cocoa_pop_demand`                                  |             |
| Added              | `global_coffee_pop_demand`                                 |             |
| Added              | `global_copper_pop_demand`                                 |             |
| Added              | `global_cotton_pop_demand`                                 |             |
| Added              | `global_dyes_pop_demand`                                   |             |
| Added              | `global_elephants_pop_demand`                              |             |
| Added              | `global_estate_satisfaction_from_legitimacy`               |             |
| Added              | `global_fiber_crops_pop_demand`                            |             |
| Added              | `global_fine_cloth_pop_demand`                             |             |
| Added              | `global_firearms_pop_demand`                               |             |
| Added              | `global_fish_pop_demand`                                   |             |
| Added              | `global_fruit_pop_demand`                                  |             |
| Added              | `global_fur_pop_demand`                                    |             |
| Added              | `global_furniture_pop_demand`                              |             |
| Added              | `global_gems_pop_demand`                                   |             |
| Added              | `global_glass_pop_demand`                                  |             |
| Added              | `global_goods_gold_pop_demand`                             |             |
| Added              | `global_heathen_pop_conversion_speed_modifier`             |             |
| Added              | `global_hellenism_religion_movement_growth_modifier`       |             |
| Added              | `global_hellenism_religion_movement_resistance_modifier`   |             |
| Added              | `global_heretic_pop_conversion_speed_modifier`             |             |
| Added              | `global_horses_pop_demand`                                 |             |
| Added              | `global_incense_pop_demand`                                |             |
| Added              | `global_iron_pop_demand`                                   |             |
| Added              | `global_ivory_pop_demand`                                  |             |
| Added              | `global_jewelry_pop_demand`                                |             |
| Added              | `global_laborers_pop_growth`                               |             |
| Added              | `global_lacquerware_pop_demand`                            |             |
| Added              | `global_lead_pop_demand`                                   |             |
| Added              | `global_leather_pop_demand`                                |             |
| Added              | `global_legumes_pop_demand`                                |             |
| Added              | `global_liquor_pop_demand`                                 |             |
| Added              | `global_livestock_pop_demand`                              |             |
| Added              | `global_lumber_pop_demand`                                 |             |
| Added              | `global_maize_pop_demand`                                  |             |
| Added              | `global_marble_pop_demand`                                 |             |
| Added              | `global_masonry_pop_demand`                                |             |
| Added              | `global_max_bureaucracy_slots`                             |             |
| Added              | `global_medicaments_pop_demand`                            |             |
| Added              | `global_mercury_pop_demand`                                |             |
| Added              | `global_migration_attraction`                              |             |
| Added              | `global_millet_pop_demand`                                 |             |
| Added              | `global_naval_supplies_pop_demand`                         |             |
| Added              | `global_nobles_pop_growth`                                 |             |
| Added              | `global_non_rural_monthly_development`                     |             |
| Added              | `global_non_rural_monthly_prosperity`                      |             |
| Added              | `global_olives_pop_demand`                                 |             |
| Added              | `global_paper_pop_demand`                                  |             |
| Added              | `global_pearls_pop_demand`                                 |             |
| Added              | `global_peasants_pop_growth`                               |             |
| Added              | `global_pepper_pop_demand`                                 |             |
| Added              | `global_porcelain_pop_demand`                              |             |
| Added              | `global_potato_pop_demand`                                 |             |
| Added              | `global_pottery_pop_demand`                                |             |
| Added              | `global_rice_pop_demand`                                   |             |
| Added              | `global_roman_culture_movement_growth_modifier`            |             |
| Added              | `global_roman_culture_movement_resistance_modifier`        |             |
| Added              | `global_saffron_pop_demand`                                |             |
| Added              | `global_salt_pop_demand`                                   |             |
| Added              | `global_saltpeter_pop_demand`                              |             |
| Added              | `global_sand_pop_demand`                                   |             |
| Added              | `global_silk_pop_demand`                                   |             |
| Added              | `global_silver_pop_demand`                                 |             |
| Added              | `global_slaves_goods_pop_demand`                           |             |
| Added              | `global_slaves_pop_growth`                                 |             |
| Added              | `global_soldiers_pop_growth`                               |             |
| Added              | `global_steel_pop_demand`                                  |             |
| Added              | `global_stone_pop_demand`                                  |             |
| Added              | `global_sugar_pop_demand`                                  |             |
| Added              | `global_tar_pop_demand`                                    |             |
| Added              | `global_tea_pop_demand`                                    |             |
| Added              | `global_tin_pop_demand`                                    |             |
| Added              | `global_tobacco_pop_demand`                                |             |
| Added              | `global_tools_pop_demand`                                  |             |
| Added              | `global_tribesmen_pop_growth`                              |             |
| Added              | `global_war_score_efficiency`                              |             |
| Added              | `global_weaponry_pop_demand`                               |             |
| Added              | `global_wheat_pop_demand`                                  |             |
| Added              | `global_wild_game_pop_demand`                              |             |
| Added              | `global_wine_pop_demand`                                   |             |
| Added              | `global_wool_pop_demand`                                   |             |
| Added              | `grant_a_triumph_cost_modifier`                            |             |
| Added              | `grant_town_rights_cost_modifier`                          |             |
| Added              | `greek_festivals_cost_modifier`                            |             |
| Added              | `honorary_titles_bureaucracy_impact_modifier`              |             |
| Added              | `host_olympiad_cost_modifier`                              |             |
| Added              | `hre_army_building_cost_modifier`                          |             |
| Added              | `hre_imperial_armory_level`                                |             |
| Added              | `imperial_senate_bureaucracy_impact_modifier`              |             |
| Added              | `implement_bureaucracy_price_cost_modifier`                |             |
| Added              | `import_efficiency`                                        |             |
| Added              | `invite_patriarch_delegation_cost_modifier`                |             |
| Added              | `jurchen_confederation_law_price_cost_modifier`            |             |
| Added              | `kephalai_bureaucracy_impact_modifier`                     |             |
| Added              | `lat_access_to_latin_reintegration_cabinet`                |             |
| Added              | `lat_access_to_reconquest_cb`                              |             |
| Added              | `loan_icon_price_cost_modifier`                            |             |
| Added              | `local_bubonic_plague_growth_modifier`                     |             |
| Added              | `local_bubonic_plague_resistance_modifier`                 |             |
| Added              | `local_burghers_estate_unrest`                             |             |
| Added              | `local_burghers_pop_growth`                                |             |
| Added              | `local_clergy_estate_unrest`                               |             |
| Added              | `local_clergy_pop_growth`                                  |             |
| Added              | `local_cloth_guild_building_levels`                        |             |
| Added              | `local_cossacks_estate_unrest`                             |             |
| Added              | `local_crown_estate_unrest`                                |             |
| Added              | `local_dhimmi_estate_unrest`                               |             |
| Added              | `local_fine_cloth_guild_building_levels`                   |             |
| Added              | `local_food_decay_modifier`                                |             |
| Added              | `local_great_pestilence_growth_modifier`                   |             |
| Added              | `local_great_pestilence_resistance_modifier`               |             |
| Added              | `local_heathen_pop_conversion_speed_modifier`              |             |
| Added              | `local_hellenism_religion_movement_growth_modifier`        |             |
| Added              | `local_hellenism_religion_movement_impact_modifier`        |             |
| Added              | `local_hellenism_religion_movement_resistance_modifier`    |             |
| Added              | `local_heretic_pop_conversion_speed_modifier`              |             |
| Added              | `local_influenza_growth_modifier`                          |             |
| Added              | `local_influenza_resistance_modifier`                      |             |
| Added              | `local_jewelry_guild_building_levels`                      |             |
| Added              | `local_laborers_pop_growth`                                |             |
| Added              | `local_malaria_growth_modifier`                            |             |
| Added              | `local_malaria_resistance_modifier`                        |             |
| Added              | `local_marketplace_building_levels`                        |             |
| Added              | `local_measles_growth_modifier`                            |             |
| Added              | `local_measles_resistance_modifier`                        |             |
| Added              | `local_merchant_capacity_modifier`                         |             |
| Added              | `local_nobles_estate_unrest`                               |             |
| Added              | `local_nobles_pop_growth`                                  |             |
| Added              | `local_peasants_estate_unrest`                             |             |
| Added              | `local_peasants_pop_growth`                                |             |
| Added              | `local_possible_town_rights`                               |             |
| Added              | `local_roman_culture_movement_growth_modifier`             |             |
| Added              | `local_roman_culture_movement_resistance_modifier`         |             |
| Added              | `local_slaves_pop_growth`                                  |             |
| Added              | `local_smallpox_growth_modifier`                           |             |
| Added              | `local_smallpox_resistance_modifier`                       |             |
| Added              | `local_soldiers_pop_growth`                                |             |
| Added              | `local_tribes_estate_unrest`                               |             |
| Added              | `local_tribesmen_pop_growth`                               |             |
| Added              | `local_typhus_growth_modifier`                             |             |
| Added              | `local_typhus_resistance_modifier`                         |             |
| Added              | `local_war_score_efficiency`                               |             |
| Added              | `magister_militum_bureaucracy_impact_modifier`             |             |
| Added              | `maintain_bureaucracy_price_cost_modifier`                 |             |
| Added              | `market_building_levels`                                   |             |
| Added              | `marriage_desirability`                                    |             |
| Added              | `max_manpower`                                             |             |
| Added              | `max_sailors`                                              |             |
| Added              | `max_siege_memory`                                         |             |
| Added              | `may_hire_eunuch_advisors`                                 |             |
| Added              | `megalopolis_upgrade_cost_modifier`                        |             |
| Added              | `mend_schism_price_cost_modifier`                          |             |
| Added              | `mercenary_maintenance_efficiency`                         |             |
| Added              | `merchant_guild_chapel_price_cost_modifier`                |             |
| Added              | `merchant_maintenance_efficiency`                          |             |
| Added              | `minimum_fort_level`                                       |             |
| Added              | `monthly_nahualt_reform_progress`                          |             |
| Added              | `monthly_towards_hellenization`                            |             |
| Added              | `monthly_towards_latinization`                             |             |
| Added              | `nahuatl_religious_actions_price_cost_modifier`            |             |
| Added              | `national_bubonic_plague_growth_modifier`                  |             |
| Added              | `national_bubonic_plague_resistance_modifier`              |             |
| Added              | `national_great_pestilence_growth_modifier`                |             |
| Added              | `national_great_pestilence_resistance_modifier`            |             |
| Added              | `national_hellenism_religion_movement_growth_modifier`     |             |
| Added              | `national_hellenism_religion_movement_resistance_modifier` |             |
| Added              | `national_influenza_growth_modifier`                       |             |
| Added              | `national_influenza_resistance_modifier`                   |             |
| Added              | `national_malaria_growth_modifier`                         |             |
| Added              | `national_malaria_resistance_modifier`                     |             |
| Added              | `national_measles_growth_modifier`                         |             |
| Added              | `national_measles_resistance_modifier`                     |             |
| Added              | `national_roman_culture_movement_growth_modifier`          |             |
| Added              | `national_roman_culture_movement_resistance_modifier`      |             |
| Added              | `national_smallpox_growth_modifier`                        |             |
| Added              | `national_smallpox_resistance_modifier`                    |             |
| Added              | `national_typhus_growth_modifier`                          |             |
| Added              | `national_typhus_resistance_modifier`                      |             |
| Added              | `navy_maintenance_efficiency`                              |             |
| Added              | `nomos_empsychos_bureaucracy_impact_modifier`              |             |
| Added              | `num_of_cataphracts_modifier`                              |             |
| Added              | `num_of_legionaries_modifier`                              |             |
| Added              | `omen_strength_modifier`                                   |             |
| Added              | `omen_time_modifier`                                       |             |
| Added              | `omens_offered`                                            |             |
| Added              | `pilgrimage_action_cost_modifier`                          |             |
| Added              | `reestablish_hellenism_price_cost_modifier`                |             |
| Added              | `remove_bureaucracy_price_cost_modifier`                   |             |
| Added              | `restore_rome_primacy_price_cost_modifier`                 |             |
| Added              | `revoke_town_rights_cost_modifier`                         |             |
| Added              | `rise_of_the_szlachta_actions_price_cost_modifier`         |             |
| Added              | `ritualistic_court_bureaucracy_impact_modifier`            |             |
| Added              | `roman_festivals_cost_modifier`                            |             |
| Added              | `romanitas_bureaucracy_impact_modifier`                    |             |
| Added              | `select_omen_god_cost_modifier`                            |             |
| Added              | `select_orthodox_education_cost_modifier`                  |             |
| Added              | `selling_efficiency`                                       |             |
| Added              | `sixty_books_of_the_basilika_bureaucracy_impact_modifier`  |             |
| Added              | `sponsor_troop_feast_cost_modifier`                        |             |
| Added              | `subject_pays_pronoia_cost_modifier`                       |             |
| Added              | `themata_bureaucracy_impact_modifier`                      |             |
| Added              | `trade_land_efficiency`                                    |             |
| Added              | `trade_sea_efficiency`                                     |             |
| Added              | `train_admiral_ability`                                    |             |
| Added              | `train_general_ability`                                    |             |
| Added              | `trust_decay`                                              |             |
| Added              | `trust_recovery`                                           |             |
| Added              | `war_score_vs_other_religion_efficiency`                   |             |
