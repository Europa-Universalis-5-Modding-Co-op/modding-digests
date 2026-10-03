# Script Documentation 1.4.0 - Beta
## Table of Contents
 * [Scopes](#scopes)
 * [Effects](#effects)
 * [Triggers](#triggers)
 * [Event Targets](#event-targets)
 * [Iterators](#iterators)
 * [On Actions](#on-actions)
## Notes
 * **Changed** means the description, scopes or anything related to the documentation for this element has changed
 * The list of iterators do **not** include generated geographic region based iterators
 * The on action scope is based on the script documentation, for more information see the `common/on_actions` directory
## Scopes
| Type | Scope | Supports Variables | Supports Effects | Supports Triggers | Save Game Identifier |
|--|--|--|--|--|--|
| Added | `expedition` | True | True | True | `expedition` |
| Added | `expedition_type` | False | True | True | `expedition_type` |
| Added | `colonial_charter_goal` | False | True | True | `colonial_charter_goal` |
| Added | `ambition` | True | True | True | `ambition` |
| Added | `ambition_definition` | False | True | True | `ambition_definition` |
| Added | `religious_order` | False | True | True | `religious_order` |
| Added | `religious_order_type` | False | True | True | `religious_order_type` |
| Added | `calling` | False | True | True | `calling` |
| Added | `industry_promotion` | False | True | True | `industry_promotion` |
| Added | `industry_type` | False | True | True | `industry_type` |
| Removed | `cardinal` | False | True | True | `cardinal` |

## Effects
| Type | Effect | Description |
|--|--|--|
| Added | `add_discriminated_culture` | Adds a discriminated culture to a country |
| Added | `add_estate_private_regiment` | Adds one unraised private regiment definition to an estate. estate = \<type\> unit_type = \<subunit_def\> |
| Added | `add_new_waypoint` | appends a new waypoint location to an active expedition's path. Also accepts a block form, add_new_waypoint = { location = x hidden = yes }, to add a waypoint whose identity is masked from the player in the route list and tooltip until it stops being hidden |
| Added | `add_political_influence` | Adds political influence |
| Added | `add_scripted_proximity_modifier_to` | Adds a scripted proximity efficiency modifier from the scope location to the target location. target = \<location\>, key = \<localizable string\>, value = \<script value\> |
| Added | `add_scripted_proximity_to` | Adds proximity from the scope location to the target location. target = \<location\>, key = \<localizable string\>, value = \<script value\> |
| Added | `add_timeline_note` | Records a world-global timeline note (key + current date) for later display on the timeline view.   |
| Added | `attach_to_religious_order` | Attaches the current location to the supplied religious order — the location becomes a holding, joining the order's location list and mirror-registering the order in the location's presence array. |
| Added | `break_betrothal` | Breaks the betrothal between character and target character |
| Added | `change_religious_order_calling` | Changes the religious order's calling to the supplied calling (must be valid for the order's type). Per-holding modifiers, projected country modifiers, holding upkeep and the order icon all switch to the new calling. |
| Added | `change_religious_order_zeal` | Modifies the religious order's global Zeal by the supplied amount (clamped 0..100). At Zeal 0 the order auto-dissolves. |
| Added | `clear_estate_private_regiments` | Clears all unraised private regiment definitions from an estate. estate = \<type\> |
| Added | `clear_expedition_waypoints` | Clears all remaining waypoints from an expedition's path. Use add_new_waypoint afterwards to set a new destination. |
| Added | `create_ambition` | Creates an ambition for a country. usage: create_ambition = { ambition_definition = \<ambition_definition\> \[any other optional parameters\] } |
| Added | `create_army_country_from_province_definition` | Creates a new army country with the current Province definition scope as capital and then scopes to the new country |
| Added | `create_betrothal` | Betrothes character to target character |
| Added | `create_location_country_from_province_definition` | Creates a new country with the current Province definition scope as capital and then scopes to the new country |
| Added | `create_navy_country_from_province_definition` | Creates a new navy country with the current Province definition scope as capital and then scopes to the new country |
| Added | `end_expedition` | Ends an active expedition immediately, firing its on_end effects. Usage: end_expedition = scope:expedition |
| Added | `expedition_return_home` | For a returns_home expedition type: starts the trip back to its origin instead of ending it outright. Usage: expedition_return_home = scope:expedition |
| Added | `fail_expedition` | Fails an active expedition immediately, firing its on_fail effects. Non-repeatable expeditions remain available to retry. Usage: fail_expedition = scope:expedition |
| Added | `found_religious_order` | Founds a new religious order of the supplied type and calling, belonging to the supplied religion, with the current location as its first holding. Optional graphical_cultures list adds extra graphical cultures to the new order. |
| Added | `grant_culture_bonus_advances` | Grants all bonus advances from a culture's definition to the country   |
| Added | `join_religious_order` | The current character becomes a member of the supplied religious order — added to the order's member roster and keeping the membership on the character for life. |
| Added | `pause_expedition` | Pauses an expedition for the given number of days. Usage: pause_expedition = 30 |
| Added | `pay_scaled_price` | Pays a fraction of a Price from a country. Usage: pay_scaled_price = { price = price:x scale = 0.2 reason = \<loc key\> } |
| Added | `press_estate_private_regiments` | Raises all unraised private regiment definitions for an estate into the country's royal army. estate = \<type\> |
| Added | `prospective_proximity_calculation` | Simulates the proximity calculation from the point of a country with capital in location. The distance are then output to a local variable map entitled map. Usage and parameters:   |
| Added | `remove_all_religious_orders` | remove_all_religious_orders = yes   |
| Added | `remove_culture_bonus_advances` | Removes all bonus advances from a culture's definition from the country   |
| Added | `remove_discriminated_culture` | Removes a discriminated culture from a country |
| Added | `remove_estate_private_regiment` | Removes one matching unraised private regiment definition from an estate. estate = \<type\> unit_type = \<subunit_def\> |
| Added | `remove_goods_import_trade_policy` | Removes the global import tariff/subvention policy for a good. Usage: remove_goods_import_trade_policy = { goods = \<goods\> } |
| Added | `remove_religious_order` | Detaches the current location from the supplied religious order — the location stops being a holding, leaving the order's location list and the location's presence array. |
| Added | `remove_scripted_proximity_from` | Removes scripted proximity from target location based on target = \<location\> and key = \<string\> |
| Added | `reset_character_location` | Moves a character back to their default location |
| Added | `reset_character_religious_figure` | stops a character being a religious figure |
| Added | `resume_expedition` | Resumes an expedition previously stalled by stall_expedition, so it can move again on its next tick. Usage: resume_expedition = scope:expedition |
| Added | `set_cabinet_action` | Sets cabinet action of this cabinet to \<type\> with scripted params |
| Added | `set_canal_open` | Opens or closes the canal passing through this location. Requires the location to be a canal through-location (registered in the adjacency CSV). |
| Added | `set_canal_restricted` | Sets the restriction flag on the canal at this location. Restricted canals only allow allies / subjects / overlords through. |
| Added | `set_character_location` | Moves a character somewhere |
| Added | `set_character_religious_figure` | Makes a character a religious figure |
| Added | `set_colonial_charter_goal` | Sets the outcome goal for a colonial charter. Usage: set_colonial_charter_goal = { target = \<charter\> goal = \<goal_key\> subject = \<country\> } |
| Added | `set_expedition_leader` | reassigns the leader of an active expedition, e.g. after the original leader's death |
| Added | `set_expedition_outcome` | Records a localization key describing how this expedition turned out, shown in the completed expeditions list.   |
| Added | `set_expedition_status_to_deviation` | Sets the expedition's status to Deviation. Usage: set_expedition_status_to_deviation = yes (scope: expedition) |
| Added | `set_expedition_status_to_in_port` | Sets the expedition's status to InPort. Usage: set_expedition_status_to_in_port = yes (scope: expedition) |
| Added | `set_expedition_status_to_traveling` | Sets the expedition's status to Traveling. Usage: set_expedition_status_to_traveling = yes (scope: expedition) |
| Added | `set_goods_export_trade_policy` | Sets a global export tariff (positive modifier) or export subvention (negative modifier) on a good. Slider range -1.0 to 1.0. Replaces any existing export policy for that good. Usage: set_goods_export_trade_policy = { goods = \<goods\> \[modifier = \<-1.0..1.0\>\] } |
| Added | `set_goods_import_trade_policy` | Sets a global import tariff (positive modifier) or import subvention (negative modifier) on a good. Slider range -1.0 to 1.0. Replaces any existing non-embargo policy for that good. Usage: set_goods_import_trade_policy = { goods = \<goods\> \[modifier = \<-1.0..1.0\>\] } |
| Added | `set_head_character` | Sets the religious order's head character to the supplied character scope (used inside on_leader_death blocks after create_character). |
| Added | `set_international_organization_icon` | Sets the illustration/icon override for an international organization, looked up under international_organization_types/specific_ios/\<icon\>.dds. Usage: set_international_organization_icon = \<icon key\> |
| Added | `set_political_influence` | Sets political influence |
| Added | `set_production_method` | Sets the production method of a building |
| Added | `set_religious_order_zeal` | Sets the religious order's global Zeal to the supplied value (clamped 0..100). Bypasses the auto-dissolve-at-zero rule used by change_religious_order_zeal. |
| Added | `set_revolt_target` | sets the original attacker of the revolt war |
| Added | `set_war_leader` | Makes the country scope the new war leader for the target war. Country must already be an active participant. Usage: set_war_leader = { war = \<war scope\> } |
| Added | `stall_expedition` | Stalls an active expedition indefinitely until resume_expedition is called on it. Usage: stall_expedition = scope:expedition |
| Added | `start_canal_construction` | Starts canal construction at the scoped location. The location must be a canal through-location. |
| Added | `start_expedition` | starts an expedition of the given type along the given path |
| Added | `start_expedition_wait_construction` | Creates a construction at the expedition's current location that the expedition waits on; on_construction_finished fires when it finishes.   |
| Changed | `add_character_modifier` | add a modifier to a character   |
| Changed | `add_cooldown` | adds a cooldown for a country, character or international organization. Usage: add_cooldown = { type = \<token\> days/weeks/months/years = \<integer\> } |
| Changed | `add_country_modifier` | add a modifier to a country   |
| Changed | `add_dynasty_modifier` | add a modifier to a dynasty   |
| Changed | `add_international_organization_modifier` | add a modifier to an international organization   |
| Changed | `add_location_modifier` | add a modifier to a location   |
| Changed | `add_movement_modifier` | add a modifier to a movement   |
| Changed | `add_province_modifier` | add a modifier to a unit   |
| Changed | `add_rebel_modifier` | add a modifier to a rebel   |
| Changed | `add_religion_modifier` | add a modifier to a unit   |
| Changed | `add_to_global_variable_list` | Adds the event target to a global variable list for the given duration   |
| Changed | `add_to_local_variable_list` | Adds the event target to a local variable list for the given duration   |
| Changed | `add_to_variable_list` | Adds the event target to a variable list on the current scope for the given duration   |
| Changed | `add_unit_modifier` | add a modifier to a unit   |
| Changed | `change_global_variable` | Changes the value of a numeric global variable   |
| Changed | `change_local_variable` | Changes the value of a numeric local variable   |
| Changed | `change_variable` | Changes the value of a numeric variable on the current scope   |
| Changed | `clamp_global_variable` | Clamps a global variable the specified max and min   |
| Changed | `clamp_local_variable` | Clamps a local variable the specified max and min   |
| Changed | `clamp_variable` | Clamps a variable the specified max and min on the current scope   |
| Changed | `clear_global_variable_list` | Empties the specified global list   |
| Changed | `clear_local_variable_list` | Empties the specified local list   |
| Changed | `clear_variable_list` | Empties the specified list on the current scope   |
| Changed | `create_character` | Creates a character for a country. The effect has the following parameters:   |
| Changed | `declare_war_with_cb` | declares a war with a specific cb  { target = \<country\> type = \<cb_type\> \[target_province = ; target_country =, character =\] } The country scope will leave all wars they fight together with the target country. |
| Changed | `end_situation` | End a situation. Usage: end_situation = \<situation\> or end_situation = { situation = \<situation\> \[outcome = "\<outcome name\>"\] }. If an outcome name is given, that outcome's immediate and effect blocks are executed and it is recorded as the situation's end outcome. |
| Changed | `hire_mercenary` | hires a mercenary for the target country. Usage: hire_mercenary = \<mercenary\> or hire_mercenary = { target = \<mercenary\> location = \<location\> } to place the hired mercenary at a specific location instead of the customer's capital |
| Changed | `post_audio_event` | Runs an audio even on a "persistent" audio object    |
| Changed | `recall_lent_unit` | Returns a lent unit to its owner (lender) and ends the loan. Does nothing if the mercenary is not a lent unit. |
| Changed | `remove_cooldown` | Removes a cooldown for a country, character or international organization. Usage: remove_cooldown = \<cooldown token\> |
| Changed | `remove_global_variable` | Removes the specified global variable   |
| Changed | `remove_list_global_variable` | Removes the target from a global variable list   |
| Changed | `remove_list_local_variable` | Removes the target from a local variable list   |
| Changed | `remove_list_variable` | Removes the target from a variable list on the current scope   |
| Changed | `remove_local_variable` | Removes the specified local variable   |
| Changed | `remove_variable` | Removes the specified variable on the current scope   |
| Changed | `round_global_variable` | Rounds a global variable to the nearest specified value   |
| Changed | `round_local_variable` | Rounds a local variable to the nearest specified value   |
| Changed | `round_variable` | Rounds a variable to the nearest specified value on the current scope   |
| Changed | `set_global_variable` | Sets a global variable   |
| Changed | `set_local_variable` | Sets a local variable   |
| Changed | `set_variable` | Sets a variable on the current scope   |
| Changed | `sort_global_variable_list` | Sorts a global variable list   |
| Changed | `sort_local_variable_list` | Sorts a local variable list   |
| Changed | `sort_variable_list` | Sorts a variable list on the current scope   |
| Removed | `add_complacency` | Adds complacency |
| Removed | `add_trust` | Adds trust (target = x value = y} |
| Removed | `set_complacency` | Sets complacency |

## Triggers
| Type | Trigger | Trait | Description |
|--|--|--|--|
| Added | `ai_country_should_colonize` | Boolean | should this country pursue colonization at all? Wealth or an eager tag, allowed by the colonisation game rule, and not a subject other than a colonial nation |
| Added | `ai_target_antagonism` | Value | Target antagonism set by ambitions. Usage: ai_target_antagonism = { target = \<object\> value \>= \<threshold\> } |
| Added | `ai_target_favours` | Value | Target favors set by ambitions. Usage: ai_target_favours = { target = \<object\> value \>= \<threshold\> } |
| Added | `ai_target_opinion` | Value | Target opinion set by ambitions. Usage: ai_target_opinion = { target = \<object\> value \>= \<threshold\> } |
| Added | `ai_target_spy_network` | Value | Target spy network set by ambitions. Usage: ai_target_spy_network = { target = \<object\> value \>= \<threshold\> } |
| Added | `ai_target_subject_loyalty` | Value | Target subject loyalty set by ambitions. Usage: ai_target_subject_loyalty = { target = \<object\> value \>= \<threshold\> } |
| Added | `ai_target_subvert` | Value | Target subvert set by ambitions. Usage: ai_target_subvert = { target = \<object\> value \>= \<threshold\> } |
| Added | `ai_target_trust` | Value | Target trust set by ambitions. Usage: ai_target_trust = { target = \<object\> value \>= \<threshold\> } |
| Added | `ai_will_select_calling` | Value | Evaluates the value of the AI selecting this particular calling. Usage: ai_will_select_calling = { calling = \<calling scope\> (location = \<location scope\> (optional)) value \<operator\> \<value\> } OR ai_will_select_calling(\<calling scope\>) OR ai_will_select_calling(\<calling scope\>\|\<location scope\>) |
| Added | `allow_female` | Boolean | checks if a succession law allows female rulers |
| Added | `allow_male` | Boolean | checks if a succession law allows male rulers |
| Added | `average_prosperity` | Value | Checks the average prosperity in the country |
| Added | `calling_is_current_of_order` |  -  | True if this calling is the supplied religious order's current calling. |
| Added | `calling_valid_for_type` |  -  | True if this calling may be adopted by the supplied religious order type (its valid_for_types includes that type). |
| Added | `can_betroth_character` |  -  | Check if the current character scope can betroth the target character |
| Added | `can_lead_expedition` | Boolean | Check if the previous-scope character meets the leader requirements for this expedition type |
| Added | `can_revoke_privilege` |  -  | Can the country declare revoke this estate privilege? can_revoke_privilege = \<privilege scope\> |
| Added | `can_start_expedition` |  -  | Check if the given country can start this expedition type. Scope: expedition_type. Value: country reference (e.g. scope:actor) |
| Added | `closeness_to_equator` | Value | Returns the value for closeness to equator for the location |
| Added | `colonize_bias` | Value | Any bias to or from this bit of geography set by ambitions. Usage: colonize_bias = { target = \<object\> value \>= \<threshold\> } |
| Added | `conquer_bias` | Value | Any bias to or from this bit of geography set by ambitions. Usage: conquer_bias = { target = \<object\> value \>= \<threshold\> } |
| Added | `country_potential_tax_base` | Value | Checks the total potential tax base of a country |
| Added | `counts_as_capital` | Boolean | Check if a location is the capital or a historical capital of its owner |
| Added | `days_difference` | Value | Returns the difference in days between two dates. Can be used is complex form (scope:first_date\|scope:second_date) or with first = and second =  |
| Added | `days_since_expedition_start` | Value | Check how many days have passed since the expedition started |
| Added | `defender_bonus` | Value | Check the defender bonus of the scope location, topography, vegetation or climate |
| Added | `diplomatic_capacity_of_new_subject` | Value | Diplomatic capacity that will be used if the country obtains this subject |
| Added | `dynamic_historical_event_fire_year` | Value | Compares the year in which a Dynamic Historical Event fired for the scoped country. Returns 0 if it never fired (or year=1 if migrated from a legacy save). Usage: dynamic_historical_event_fire_year = { event = \<event_key\> value \<comparator\> \<year\> } |
| Added | `dynamic_historical_event_fired` |  -  | Checks whether a Dynamic Historical Event has fired for the scoped country. Usage: dynamic_historical_event_fired = \<event_key\> |
| Added | `estate_raised_regiment_count` | Value | Checks the number of raised (in-service) private regiment references for an estate. Country scope requires estate = \<type\>. |
| Added | `estate_total_regiment_count` | Value | Checks the total (unraised + raised) private regiment count for an estate. Country scope requires estate = \<type\>. |
| Added | `estate_unraised_regiment_count` | Value | Checks the number of unraised private regiment definitions for an estate. Country scope requires estate = \<type\>. |
| Added | `estimated_loot_income` | Value | Check how much gold a country would gain from looting the scope location.  |
| Added | `expedition_is_in_deviation` | Boolean | Check if an expedition is in deviation |
| Added | `expedition_is_in_port` | Boolean | Check if an expedition is currently stopped at a waypoint |
| Added | `expedition_is_paused` | Boolean | Check if an expedition is currently paused (e.g. pause_expedition is still in effect) |
| Added | `expedition_is_returning` | Boolean | Check if an expedition is on its return leg (returns_home appended the trip back) |
| Added | `expedition_is_stalled` | Boolean | Check if an expedition is currently stalled (i.e. stall_expedition was called and resume_expedition has not yet been called) |
| Added | `expedition_is_traveling` | Boolean | Check if an expedition is currently traveling between waypoints |
| Added | `expedition_is_waiting_on_construction` | Boolean | Check if an expedition is currently waiting on a start_expedition_wait_construction construction to finish |
| Added | `expedition_start_utility` | Value | Utility score for starting an expedition type from a country scope. Usage: expedition_start_utility = { expedition_type = \<type\> value \>= \<threshold\> } |
| Added | `expedition_wait_construction_has_goods_demand` |  -  | Check if the expedition's current start_expedition_wait_construction has the given goods_demand. Usage: expedition_wait_construction_has_goods_demand = my_goods_demand_key (scope: expedition) |
| Added | `explore_bias` | Value | Any bias to or from this bit of geography set by ambitions. Usage: explore_bias = { target = \<object\> value \>= \<threshold\> } |
| Added | `first_name_starts_with_vowel` | Boolean | Display only, never use in synced script: resolves the character's first name in the display language, so it can differ between machines. Checks if that name begins with a vowel (or a mute h where the language elides before one) |
| Added | `formable_level` | Value | Checks if a country has a certain formable level |
| Added | `has_active_disaster` |  -  | Does the country have an active disaster of the given type? Usage: has_active_disaster = disaster_type:\<disaster type\> |
| Added | `has_any_disease_trait` | Boolean | character has a health trait that can kill them (a disease like smallpox, not an injury like one_eyed) |
| Added | `has_any_religious_order_presence` | Boolean | True if at least one religious order of the country's religion holds a location in this country. |
| Added | `has_any_visible_situation` | Boolean | country can see at least one active situation (the situation's visible block passes for it) |
| Added | `has_canal_construction` | Boolean | Is the location building a canal? |
| Added | `has_competing_foreign_buildings_with` |  -  | Does this country own a foreign building in, or adjacent to, a location where the target country also owns a foreign building? |
| Added | `has_country_religious_schools` | Boolean | countries of this religion belong to a religious school |
| Added | `has_discriminated_culture` |  -  | Check if a country has a culture as a Discriminated culture |
| Added | `has_gfx_tag` |  -  | Checks if the unit type has a specific gfx tag |
| Added | `has_goods_export_trade_policy` |  -  | Checks if the scope country has an active global export trade policy (tariff or subvention) set for a good. Usage: has_goods_export_trade_policy = { goods = \<goods\> } |
| Added | `has_goods_import_trade_policy` |  -  | Checks if the scope country has an active global import trade policy (tariff or subvention) set for a good. Usage: has_goods_import_trade_policy = { goods = \<goods\> } |
| Added | `has_industry_promotion` |  -  | Checks if a country has an active industry promotion of a specific industry_type |
| Added | `has_leader_requirements` | Boolean | True if the expedition type defines a leader trigger block |
| Added | `has_new_royal_marriage_with` |  -  | Does the country have a royal marriage with the specified country that was formed after the game started, as opposed to one already in place from the historical starting setup? |
| Added | `has_non_rural_port` | Boolean | Checks if a country has at least one non-rural port |
| Added | `has_religious_orders` | Boolean | True if this religion has at least one religious order registered to it. |
| Added | `has_scripted_proximity_to` |  -  | Check if a location has scripted proximity to the target location of the specified key. Usage: has_scripted_proximity_to = { target = \<target location\> key = \<key of scripted proximity\> } |
| Added | `hre_election_vote_score` | Value | How much the voter wants to elect the scope country as leader of the supplied international organization. Usage: hre_election_vote_score = { international_organization = \<international organization\> voter = \<country\> resolution = \<resolution\> value \<operator\> \<value\> } or hre_election_vote_score(\<international organization\>\|\<voter\>\|\<resolution\>) |
| Added | `industry_best_area_income` | Value | gets the monthly income a country has in its highest-income area for this industry_type - industry_best_area_income = { country = \<country\> value \>\<= \<value\> } |
| Added | `industry_best_area_levels` | Value | gets the building levels a country has in its highest-income area for this industry_type - industry_best_area_levels = { country = \<country\> value \>\<= \<value\> } |
| Added | `industry_best_area_tax_base` | Value | gets the tax base a country has in its highest-income area for this industry_type - industry_best_area_tax_base = { country = \<country\> value \>\<= \<value\> } |
| Added | `industry_building_levels_in_area` | Value | gets the total building levels a country has in an area producing the goods of an industry_type - industry_building_levels_in_area = { country = \<country\> industry_type = \<industry_type\> value \>\<= \<value\> } |
| Added | `industry_income_in_area` | Value | gets the total monthly income a country has in an area from buildings producing the goods of an industry_type - industry_income_in_area = { country = \<country\> industry_type = \<industry_type\> value \>\<= \<value\> } |
| Added | `industry_tax_base_in_area` | Value | gets the total tax base a country has in an area from buildings producing the goods of an industry_type - industry_tax_base_in_area = { country = \<country\> industry_type = \<industry_type\> value \>\<= \<value\> } |
| Added | `is_betrothed` | Boolean | character is betrothed to someone |
| Added | `is_canal_open` | Boolean | Returns true if the canal at this location is built and open. |
| Added | `is_canal_restricted` | Boolean | Returns true if the canal owner has restricted passage to allies and subjects only. |
| Added | `is_discriminated_in` |  -  | If a culture is discriminated in the target country? |
| Added | `is_eligible_for_betrothal` | Boolean | Check if the current character scope can betroth someone |
| Added | `is_eligible_for_royal_betrothal` | Boolean | if character is eligible for betrothal. Is more restrictive and focused on rulers / heirs than the can_marry trigger |
| Added | `is_estate_private_regiment` | Boolean | subunit was raised from an estate private army |
| Added | `is_expedition_leader` | Boolean | Check if a character is currently leading an expedition |
| Added | `is_formable_visible` |  -  | Checks if the country can even see the formable of the formable country in the first place. |
| Added | `is_frozen` | Boolean | Check if a location is currently frozen over |
| Added | `is_goods_valid_for_location` |  -  | Checks if a specific goods can be the raw material in the scope location |
| Added | `is_head_of_religious_order_type` |  -  | True if this character is the head (Grand Master) of any religious order whose type matches the supplied religious_order_type — used to exempt military-order heads from the clergy-estate 'no armor' portrait restriction. |
| Added | `is_heir_of_court_country` | Boolean | character is Heir of their court country |
| Added | `is_holding_of_any_religious_order` | Boolean | True if this location has at least one religious order with presence (i.e. is a holding). |
| Added | `is_host` | Boolean | Is this country player the host of a session multiplayer? |
| Added | `is_in_defensive_war` | Boolean | Country is a defender in any of its current wars. |
| Added | `is_location_valid_for_goods` |  -  | Checks if the scope goods can be the raw material in the supplied location |
| Added | `is_production_method_locked` | Boolean | Checks if a building has its production method locked |
| Added | `is_proximity_source` | Boolean | Check if a location is a source of proximity |
| Added | `is_religious_order_member` | Boolean | True if this character is (or was in life) a member of any religious order. |
| Added | `is_south_of` |  -  | Check if a location is south of another location |
| Added | `is_unit_type` |  -  | Checks if the unit type scope is a specific unit type |
| Added | `is_valid_subject_for_goal` |  -  | Whether the country is a valid subject for the given colonial charter goal |
| Added | `is_waypoint_in_expedition` |  -  | Check if a location is a waypoint of the target expedition. Scope: location. Value: expedition reference (e.g. scope:target_expedition) |
| Added | `land_war_attrition_casualties` | Value | Amount of land casualties taken by the country in this war due to attrition "scope:war.land_war_attrition_casualties(c:FRA)" |
| Added | `land_war_battle_casualties` | Value | Amount of land casualties taken by the country in this war due to battle "scope:war.land_war_battle_casualties(c:FRA)" |
| Added | `land_war_capture_casualties` | Value | Amount of land casualties taken by the country in this war due to capture "scope:war.land_war_capture_casualties(c:FRA)" |
| Added | `land_war_casualties` | Value | Amount of land casualties taken by the country in this war "scope:war.land_war_casualties(c:FRA)" |
| Added | `land_war_disease_casualties` | Value | Amount of land casualties taken by the country in this war due to disease "scope:war.land_war_disease_casualties(c:FRA)" |
| Added | `last_months_balance` | Value | Checks the last realized monthly balance of a country. Zero until a first month has been processed |
| Added | `location_highest_work_of_art_quality` | Value | Checks the quality of the highest-quality work of art in a location |
| Added | `location_holy_site_importance` | Value | Importance of the most important holy site in the location |
| Added | `location_potential_tax_base` | Value | Checks the potential tax-base of a location |
| Added | `location_valid_for_calling` |  -  | True if this location satisfies the supplied calling's location_trigger requirements and the founding-location requirements of the calling's order type— used to gate where the calling's holdings may be seated, both when founding an order and when adding a holding. |
| Added | `location_valid_for_religious_order_type` |  -  | True if this location satisfies the supplied religious order type's default founding-location requirements (owner / region / frontier). |
| Added | `lowest_war_strength_balance` | Value | Checks the lowest war strength balance of ongoing wars |
| Added | `loyalty_from_subject_bloc_strength` | Value | Checks the loyalty change from subject bloc with same subject types. Usage: loyalty_from_subject_bloc_strength = { type = \<subject type\> value \<operator\> \<value\> } or loyalty_from_subject_bloc_strength(\<subject type\>) |
| Added | `maritime_presence_bias` | Value | Any bias to or from this bit of geography set by ambitions. Usage: maritime_presence_bias = { target = \<object\> value \>= \<threshold\> } |
| Added | `max_age` |  -  | Checks if the unit type's age is the given age or earlier |
| Added | `min_age` |  -  | Checks if the unit type's age is the given age or later |
| Added | `monthly_minting_inflation` | Value | Actual monthly inflation currently generated by minting |
| Added | `monthly_political_influence` | Value | Return the amount of political influence the country gains per month |
| Added | `months_difference` | Value | Returns the difference in months between two dates. Can be used is complex form (scope:first_date\|scope:second_date) or with first = and second =  |
| Added | `navy_war_attrition_casualties` | Value | Amount of naval casualties taken by the country in this war due to attrition "scope:war.navy_war_attrition_casualties(c:FRA)" |
| Added | `navy_war_battle_casualties` | Value | Amount of naval casualties taken by the country in this war due to battle "scope:war.navy_war_battle_casualties(c:FRA)" |
| Added | `navy_war_capture_casualties` | Value | Amount of naval casualties taken by the country in this war due to capture "scope:war.navy_war_capture_casualties(c:FRA)" |
| Added | `navy_war_casualties` | Value | Amount of naval casualties taken by the country in this war "scope:war.navy_war_casualties(c:FRA)" |
| Added | `navy_war_disease_casualties` | Value | Amount of naval casualties taken by the country in this war due to disease "scope:war.navy_war_disease_casualties(c:FRA)" |
| Added | `needs_subject` | Boolean | Whether this charter goal requires a subject country to be selected |
| Added | `num_cbs` | Value | Checks if a country has a certain amount of CBs |
| Added | `num_locations_in_religious_order` | Value | The number of holdings this religious order holds worldwide. |
| Added | `num_order_holdings` | Value | The number of this country's owned locations that are religious order holdings. |
| Added | `num_order_holdings_of_order` | Value | The number of this country's owned locations that are holdings to the target religious order. Usage: num_order_holdings_of_order = { religious_order = \<religious order scope\> value \<comparator\> \<int\> } or num_order_holdings_of_order(\<religious order scope\>) |
| Added | `object_bias` | Value | Any bias to or from this object set by ambitions. Usage: object_bias = { target = \<object\> value \>= \<threshold\> } |
| Added | `political_influence` | Value | How much political influence does the country have? |
| Added | `political_influence_percentage` | Value | How high the percentage of the current political influence compared to the maximum does the country have? |
| Added | `province_average_population` | Value | Checks the average population per location of a province |
| Added | `religious_order_average_holding_prosperity` | Value | The mean prosperity across this religious order's holdings, in the -1 to 1 prosperity range. |
| Added | `religious_order_type_foundable_by` |  -  | True if the supplied country satisfies this religious order type's default founding-country requirements (e.g. religion). |
| Added | `religious_order_zeal` | Value | The religious order's global Zeal value 0-100 (the survival meter). At 0 the order is auto-dissolved. |
| Added | `rgo_profit` | Value | Checks a location's raw goods profit per RGO level |
| Added | `should_consider_court_language_change` | Boolean | AI-only cheap precheck: could the country plausibly benefit from changing its court language? |
| Added | `total_discriminated_culture_population` | Value | Checks if a country has a discriminated culture population size of the specified value |
| Added | `trade_capacity` | Value | How much trade capacity is used by this trade? |
| Added | `transport_cost` | Value | Returns the transport cost of the goods scope.  |
| Added | `tutorial_balance` | Value | Calculates the current monthly balance live. Expensive: only for tutorial lessons, never in AI weights or mass-evaluated triggers |
| Added | `unit_category` |  -  | Checks if the unit type belongs to a specific unit category |
| Added | `uses_exterior_background` | Boolean | character uses the exterior illustration background variant |
| Added | `war_casualties` | Value | Amount of casualties taken by a side in this war.   |
| Added | `war_participation` | Value | The real participation score (a percent, 0..1) of the current country scope in the target war. Usage: war_participation = { war = \<war scope\> value = \<script value\> } or war_participation(\<war scope\>) |
| Added | `would_be_overseas_for` |  -  | Check if a location would be overseas for the given country |
| Added | `years_difference` | Value | Returns the difference in years between two dates. Can be used is complex form (scope:first_date\|scope:second_date) or with first = and second =  |
| Added | `years_since_game_start` | Value | Compare the number of years elapsed since the game started |
| Changed | `can_upgrade_subunit` | Boolean | returns trus if the subunit can be upgraded |
| Changed | `gfx_culture_applicable` |  -  | Checks if a culture gfx applies to the scope object |
| Changed | `global_variable_list_size` |  -  | Checks the size of a global variable list   |
| Changed | `has_cooldown` |  -  | Does a country, character or international organization have a particular cooldown active |
| Changed | `has_fired_unique_event` |  -  | Checks if the game has already fired the unique event. For DHEs, evaluated per-country on the current scope's country; for non-DHE fire_only_once events, evaluated globally. |
| Changed | `has_global_variable` |  -  | Checks whether the specified global variable is set.   |
| Changed | `has_global_variable_list` |  -  | Checks whether the specified global variable list is set   |
| Changed | `has_local_variable` |  -  | Checks whether the specified local variable is set.   |
| Changed | `has_local_variable_list` |  -  | Checks whether the specified local variable list is set   |
| Changed | `has_variable` |  -  | Checks whether the current scope has the specified variable set.   |
| Changed | `heir_candidates_count` | Value | Checks amount of heir candidates in an heir selection for a country. Usage - heir_candidates_count = { country = x value \[operator\] y } or heir_candidates_count(country) |
| Changed | `is_key_in_global_variable_map` |  -  | Checks if a target is a key in a global variable map   |
| Changed | `is_key_in_local_variable_map` |  -  | Checks if a target is a key in a local variable map   |
| Changed | `is_key_in_variable_map` |  -  | Checks if a target is a key in a variable map   |
| Changed | `is_target_in_global_variable_list` |  -  | Checks if a target is in a global variable list   |
| Changed | `is_target_in_local_variable_list` |  -  | Checks if a target is in a local variable list   |
| Changed | `is_target_in_variable_list` |  -  | Checks if a target is in a variable list on the current scope   |
| Changed | `is_value_in_global_variable_map` |  -  | Checks if a target is a value in a global variable map   |
| Changed | `is_value_in_local_variable_map` |  -  | Checks if a target is a value in a local variable map   |
| Changed | `is_value_in_variable_map` |  -  | Checks if a target is a value in a variable map   |
| Changed | `local_variable_list_size` |  -  | Checks the size of a local variable list   |
| Changed | `monthly_balance` | Value | Checks the last realized monthly balance of a country. Zero until a first month has been processed. Alias of last_months_balance |
| Changed | `trade_capacity_usage_percent` | Value | How much of the assigned capacity is being used? (%) |
| Changed | `variable_list_size` |  -  | Checks the size of a variable list on the current scope   |
| Removed | `complacency` | Value | How much complacency does the country/IO have? |
| Removed | `complacency_percentage` | Value | How high the percentage of the current complacency compared to the maximum does the country/IO have? |
| Removed | `has_ai_disposition_toward_player` |  -  | Does the country view the player with the given AI disposition? (alarmed/wary/planning_war/covets/domineering/rivals/indifferent/friendly) |

## Event Targets
| Type | Event Target | Description |
|--|--|--|
| Added | `assimilating_culture` | Unknown, add something in code registration |
| Added | `naturally_assimilating_culture` | Unknown, add something in code registration |
| Added | `industry_type` | Unknown, add something in code registration |
| Added | `assimilating_from_culture` | Unknown, add something in code registration |
| Added | `type` | Gets the unit type of a subunit |
| Added | `top_overlord_in_war` | Links to whoever is the supplied country's top overlord in the scope war (on their side). Usage: top_overlord_in_war:\<country\> or top_overlord_in_war(\<country\>) |
| Added | `ambition_definition` | Unknown, add something in code registration |
| Added | `calling` | Unknown, add something in code registration |
| Added | `expedition_type` | Unknown, add something in code registration |
| Added | `industry_type` | Unknown, add something in code registration |
| Added | `religious_order_type` | Unknown, add something in code registration |
| Added | `ambition_definition` | Unknown, add something in code registration |
| Added | `religious_order` | Unknown, add something in code registration |
| Added | `order_calling` | Unknown, add something in code registration |
| Added | `order_type` | Unknown, add something in code registration |
| Added | `concession_policy` | Unknown, add something in code registration |
| Added | `concession_privilege` | Unknown, add something in code registration |
| Added | `removal_price_modifier` | Unknown, add something in code registration |
| Added | `expedition_current_location` | Unknown, add something in code registration |
| Added | `expedition_leader` | Unknown, add something in code registration |
| Added | `expedition_owner` | Unknown, add something in code registration |
| Added | `expedition_type` | Unknown, add something in code registration |

## Iterators
| Type | Iterator |
|--|--|
| Added | `{any\|every\|ordered\|random}_betrothal` |
| Added | `{any\|every\|ordered\|random}_calling` |
| Added | `{any\|every\|ordered\|random}_character_in_order` |
| Added | `{any\|every\|ordered\|random}_colonial_charter_goal` |
| Added | `{any\|every\|ordered\|random}_country_borrowed_from` |
| Added | `{any\|every\|ordered\|random}_country_including_inactive` |
| Added | `{any\|every\|ordered\|random}_country_wants_casus_belli_with` |
| Added | `{any\|every\|ordered\|random}_country_wants_military_access_in` |
| Added | `{any\|every\|ordered\|random}_country_wants_to_attack` |
| Added | `{any\|every\|ordered\|random}_country_wants_to_subjugate` |
| Added | `{any\|every\|ordered\|random}_discriminated_culture` |
| Added | `{any\|every\|ordered\|random}_expedition` |
| Added | `{any\|every\|ordered\|random}_expedition_type` |
| Added | `{any\|every\|ordered\|random}_location_in_religious_order` |
| Added | `{any\|every\|ordered\|random}_order_holding_in_country` |
| Added | `{any\|every\|ordered\|random}_potential_expansion_target` |
| Added | `{any\|every\|ordered\|random}_religious_order` |
| Added | `{any\|every\|ordered\|random}_religious_order_in_country` |
| Added | `{any\|every\|ordered\|random}_religious_order_in_location` |
| Added | `{any\|every\|ordered\|random}_religious_order_in_religion` |
| Added | `{any\|every\|ordered\|random}_religious_order_type` |

## Modifiers
| Type | Modifier | Scope |
|--|--|--|
| Added | `estate_emergency_action_cost_modifier` | Country |
| Added | `ask_for_extra_levies_cost_modifier` | Country |
| Added | `extraordinary_taxes_cost_modifier` | Country |
| Added | `ask_clergy_for_legitimacy_cost_modifier` | Country |
| Added | `ask_nobility_for_diplomats_cost_modifier` | Country |
| Added | `ask_burghers_for_loan_cost_modifier` | Country |
| Added | `ask_commoners_for_stability_cost_modifier` | Country |
| Added | `ask_tribes_for_manpower_cost_modifier` | Country |
| Added | `invite_religious_order_price_cost_modifier` | Country |
| Added | `found_religious_order_price_cost_modifier` | Country |
| Added | `cabalgada_raids_price_cost_modifier` | Country |
| Added | `feed_the_poor_price_cost_modifier` | Country |
| Added | `bless_the_banners_price_cost_modifier` | Country |
| Added | `escort_the_sea_lanes_price_cost_modifier` | Country |
| Added | `entrust_the_chancery_price_cost_modifier` | Country |
| Added | `pray_for_the_realm_price_cost_modifier` | Country |
| Added | `open_the_scriptoria_price_cost_modifier` | Country |
| Added | `break_new_ground_price_cost_modifier` | Country |
| Added | `preach_a_mission_price_cost_modifier` | Country |
| Added | `absolve_the_court_price_cost_modifier` | Country |
| Added | `change_order_calling_price_cost_modifier` | Country |
| Added | `expel_order_holding_price_cost_modifier` | Country |
| Added | `local_food_preservation_efficiency_modifier` | Location |
| Added | `vacate_cabinet_for_command_cost_modifier` | Country |
| Added | `add_discriminated_culture_cost_modifier` | Country |
| Added | `remove_discriminated_culture_cost_modifier` | Country |
| Added | `subject_pays_familial_governor_cost_modifier` | Country |
| Added | `can_promote_industry` | Country |
| Added | `possible_industry_promotions` | Country |
| Added | `character_mil_child_education_modifier` | Character |
| Added | `character_dip_child_education_modifier` | Character |
| Added | `character_adm_child_education_modifier` | Character |
| Added | `character_child_education_modifier` | Character |
| Added | `minimum_num_local_governors` | Country |
| Added | `num_ostrogs` | Country |
| Added | `num_lieutenancy` | Country |
| Added | `monthly_political_influence` | Country |
| Added | `monthly_political_influence_gain_modifier` | Country |
| Added | `global_free_building_levels_modifier` | Country |
| Added | `global_monthly_development_modifier` | Country |
| Added | `sea_land_transition_cost_distance_from_capital` | Country |
| Added | `grant_industry_promotion_cost_modifier` | Country |
| Added | `upgrade_town_rights_cost_modifier` | Country |
| Added | `local_food_production_mult` | Location |
| Added | `movement_blocked` | Location |
| Added | `can_extract_camels` | Country |
| Added | `ban_exports_of_camels` | Country |
| Added | `ban_imports_of_camels` | Country |
| Added | `local_camels_output_modifier` | Location |
| Added | `local_wine_establishment_speed` | Location |
| Added | `local_tar_establishment_speed` | Location |
| Added | `local_porcelain_establishment_speed` | Location |
| Added | `local_naval_supplies_establishment_speed` | Location |
| Added | `local_weaponry_establishment_speed` | Location |
| Added | `local_glass_establishment_speed` | Location |
| Added | `local_steel_establishment_speed` | Location |
| Added | `local_cloth_establishment_speed` | Location |
| Added | `local_fine_cloth_establishment_speed` | Location |
| Added | `local_liquor_establishment_speed` | Location |
| Added | `local_beer_establishment_speed` | Location |
| Added | `local_paper_establishment_speed` | Location |
| Added | `local_books_establishment_speed` | Location |
| Added | `local_jewelry_establishment_speed` | Location |
| Added | `local_leather_establishment_speed` | Location |
| Added | `local_tools_establishment_speed` | Location |
| Added | `local_lacquerware_establishment_speed` | Location |
| Added | `global_camels_output_modifier` | Country |
| Added | `global_wine_establishment_speed` | Country |
| Added | `global_tar_establishment_speed` | Country |
| Added | `global_porcelain_establishment_speed` | Country |
| Added | `global_naval_supplies_establishment_speed` | Country |
| Added | `global_weaponry_establishment_speed` | Country |
| Added | `global_glass_establishment_speed` | Country |
| Added | `global_steel_establishment_speed` | Country |
| Added | `global_cloth_establishment_speed` | Country |
| Added | `global_fine_cloth_establishment_speed` | Country |
| Added | `global_liquor_establishment_speed` | Country |
| Added | `global_beer_establishment_speed` | Country |
| Added | `global_paper_establishment_speed` | Country |
| Added | `global_books_establishment_speed` | Country |
| Added | `global_jewelry_establishment_speed` | Country |
| Added | `global_leather_establishment_speed` | Country |
| Added | `global_tools_establishment_speed` | Country |
| Added | `global_lacquerware_establishment_speed` | Country |
| Added | `mercenary_cost_for_enemies` | Country |
| Added | `mercenary_payment_to_owner` | Country |
| Added | `tariff_impact_on_price` | Country |
| Added | `max_tariff` | Country |
| Added | `max_trade_subventions` | Country |
| Added | `tariff_income` | Country |
| Added | `local_firearms_establishment_speed` | Location |
| Added | `global_firearms_establishment_speed` | Country |
| Added | `local_cannons_establishment_speed` | Location |
| Added | `global_cannons_establishment_speed` | Country |
| Added | `local_masonry_establishment_speed` | Location |
| Added | `global_masonry_establishment_speed` | Country |
| Added | `local_pottery_establishment_speed` | Location |
| Added | `global_pottery_establishment_speed` | Country |
| Added | `local_furniture_establishment_speed` | Location |
| Added | `global_furniture_establishment_speed` | Country |
| Added | `character_mortality_chance_by_bubonic_plague` | Country |
| Added | `global_life_expectancy_squared` | Country |
| Added | `casualty_pop_losses` | Country |
| Added | `local_egyptian_plague_impact_modifier` | Location |
| Added | `national_egyptian_plague_resistance_modifier` | Country |
| Added | `local_egyptian_plague_resistance_modifier` | Location |
| Added | `national_egyptian_plague_growth_modifier` | Country |
| Added | `local_egyptian_plague_growth_modifier` | Location |
| Added | `mobilize_the_shurat_price_cost_modifier` | Country |
| Added | `elect_imam_price_cost_modifier` | Country |
| Added | `inheritance_contract_cost_cost_modifier` | Country |
| Added | `characters_use_country_coa` | Country |
| Added | `offer_cardinal_seat_for_crusade_price_cost_modifier` | Country |
| Added | `offer_recognition_for_jihad_price_cost_modifier` | Country |
| Added | `preach_the_crusade_price_cost_modifier` | Country |
| Added | `issue_a_fatwa_price_cost_modifier` | Country |
| Added | `proclaim_jihad_privileges_price_cost_modifier` | Country |
| Added | `grant_indulgence_price_cost_modifier` | Country |
| Added | `promise_of_martyrdom_price_cost_modifier` | Country |
| Added | `convert_occupied_territory_price_cost_modifier` | Country |
| Added | `hasten_holy_war_preparations_price_cost_modifier` | Country |
| Added | `petition_for_the_bula_de_cruzada_price_cost_modifier` | Country |
| Added | `summon_iberian_military_orders_price_cost_modifier` | Country |
| Added | `summon_volunteers_of_the_faith_price_cost_modifier` | Country |
| Added | `crusade_treasury_contribution_price_cost_modifier` | Country |
| Added | `jihad_treasury_contribution_price_cost_modifier` | Country |
| Added | `global_camels_pop_demand` | Country |
| Added | `local_market_upgrade_building_levels` | Location |
| Added | `tribes_estate_allowed_noble_marriage` | Country |
| Added | `cossacks_estate_allowed_noble_marriage` | Country |
| Added | `crown_estate_allowed_noble_marriage` | Country |
| Added | `nobles_estate_allowed_noble_marriage` | Country |
| Added | `clergy_estate_allowed_noble_marriage` | Country |
| Added | `burghers_estate_allowed_noble_marriage` | Country |
| Added | `peasants_estate_allowed_noble_marriage` | Country |
| Added | `dhimmi_estate_allowed_noble_marriage` | Country |
| Added | `decline_of_empire_actions_price_cost_modifier` | Country |
| Added | `crusade_spiritual_leader_can_participate_in_parliament` | InternationalOrganization |
| Added | `crusade_spiritual_leader_agenda_impact` | InternationalOrganization |
| Added | `crusade_temporal_leader_can_participate_in_parliament` | InternationalOrganization |
| Added | `crusade_temporal_leader_agenda_impact` | InternationalOrganization |
| Added | `jihad_spiritual_leader_can_participate_in_parliament` | InternationalOrganization |
| Added | `jihad_spiritual_leader_agenda_impact` | InternationalOrganization |
| Added | `oligarchic_capture_disaster_actions_price_cost_modifier` | Country |
| Added | `crisis_of_faith_disaster_actions_price_cost_modifier` | Country |
| Added | `camels_impacts_inflation` | Country |
| Added | `camels_used_for_minting` | Country |
| Added | `enable_religious_courts` | Country |
| Added | `may_use_integrate_area_cabinet_action` | Country |
| Added | `allow_ibadi_majlis_ammi_said_council_parliament` | Country |
| Added | `start_expedition_cost_modifier` | Country |
| Added | `nobles_estate_allowed_private_army` | Country |
| Added | `burghers_estate_allowed_private_army` | Country |
| Added | `clergy_estate_allowed_private_army` | Country |
| Added | `peasants_estate_allowed_private_army` | Country |
| Added | `cossacks_estate_allowed_private_army` | Country |
| Added | `crown_estate_allowed_private_army` | Country |
| Added | `dhimmi_estate_allowed_private_army` | Country |
| Added | `tribes_estate_allowed_private_army` | Country |
| Added | `ambition_slots` | Country |
| Added | `contesting_ambition_slots` | Country |
| Added | `local_horses_establishment_speed` | Location |
| Added | `global_horses_establishment_speed` | Country |
| Added | `local_clay_establishment_speed` | Location |
| Added | `global_clay_establishment_speed` | Country |
| Added | `local_sand_establishment_speed` | Location |
| Added | `global_sand_establishment_speed` | Country |
| Added | `local_coal_establishment_speed` | Location |
| Added | `global_coal_establishment_speed` | Country |
| Added | `local_iron_establishment_speed` | Location |
| Added | `global_iron_establishment_speed` | Country |
| Added | `local_copper_establishment_speed` | Location |
| Added | `global_copper_establishment_speed` | Country |
| Added | `local_goods_gold_establishment_speed` | Location |
| Added | `global_goods_gold_establishment_speed` | Country |
| Added | `local_silver_establishment_speed` | Location |
| Added | `global_silver_establishment_speed` | Country |
| Added | `local_stone_establishment_speed` | Location |
| Added | `global_stone_establishment_speed` | Country |
| Added | `local_tin_establishment_speed` | Location |
| Added | `global_tin_establishment_speed` | Country |
| Added | `local_lead_establishment_speed` | Location |
| Added | `global_lead_establishment_speed` | Country |
| Added | `local_silk_establishment_speed` | Location |
| Added | `global_silk_establishment_speed` | Country |
| Added | `local_dyes_establishment_speed` | Location |
| Added | `global_dyes_establishment_speed` | Country |
| Added | `local_incense_establishment_speed` | Location |
| Added | `global_incense_establishment_speed` | Country |
| Added | `local_tea_establishment_speed` | Location |
| Added | `global_tea_establishment_speed` | Country |
| Added | `local_cocoa_establishment_speed` | Location |
| Added | `global_cocoa_establishment_speed` | Country |
| Added | `local_coffee_establishment_speed` | Location |
| Added | `global_coffee_establishment_speed` | Country |
| Added | `local_fiber_crops_establishment_speed` | Location |
| Added | `global_fiber_crops_establishment_speed` | Country |
| Added | `local_ivory_establishment_speed` | Location |
| Added | `global_ivory_establishment_speed` | Country |
| Added | `local_lumber_establishment_speed` | Location |
| Added | `global_lumber_establishment_speed` | Country |
| Added | `local_salt_establishment_speed` | Location |
| Added | `global_salt_establishment_speed` | Country |
| Added | `local_medicaments_establishment_speed` | Location |
| Added | `global_medicaments_establishment_speed` | Country |
| Added | `local_gems_establishment_speed` | Location |
| Added | `global_gems_establishment_speed` | Country |
| Added | `local_pearls_establishment_speed` | Location |
| Added | `global_pearls_establishment_speed` | Country |
| Added | `local_amber_establishment_speed` | Location |
| Added | `global_amber_establishment_speed` | Country |
| Added | `local_saltpeter_establishment_speed` | Location |
| Added | `global_saltpeter_establishment_speed` | Country |
| Added | `local_alum_establishment_speed` | Location |
| Added | `global_alum_establishment_speed` | Country |
| Added | `local_elephants_establishment_speed` | Location |
| Added | `global_elephants_establishment_speed` | Country |
| Added | `local_marble_establishment_speed` | Location |
| Added | `global_marble_establishment_speed` | Country |
| Added | `local_mercury_establishment_speed` | Location |
| Added | `global_mercury_establishment_speed` | Country |
| Added | `local_saffron_establishment_speed` | Location |
| Added | `global_saffron_establishment_speed` | Country |
| Added | `local_pepper_establishment_speed` | Location |
| Added | `global_pepper_establishment_speed` | Country |
| Added | `local_cloves_establishment_speed` | Location |
| Added | `global_cloves_establishment_speed` | Country |
| Added | `local_chili_establishment_speed` | Location |
| Added | `global_chili_establishment_speed` | Country |
| Added | `local_wool_establishment_speed` | Location |
| Added | `global_wool_establishment_speed` | Country |
| Added | `local_cotton_establishment_speed` | Location |
| Added | `global_cotton_establishment_speed` | Country |
| Added | `local_sugar_establishment_speed` | Location |
| Added | `global_sugar_establishment_speed` | Country |
| Added | `local_tobacco_establishment_speed` | Location |
| Added | `global_tobacco_establishment_speed` | Country |
| Added | `local_wild_game_establishment_speed` | Location |
| Added | `global_wild_game_establishment_speed` | Country |
| Added | `local_fur_establishment_speed` | Location |
| Added | `global_fur_establishment_speed` | Country |
| Added | `local_fish_establishment_speed` | Location |
| Added | `global_fish_establishment_speed` | Country |
| Added | `local_wheat_establishment_speed` | Location |
| Added | `global_wheat_establishment_speed` | Country |
| Added | `local_maize_establishment_speed` | Location |
| Added | `global_maize_establishment_speed` | Country |
| Added | `local_rice_establishment_speed` | Location |
| Added | `global_rice_establishment_speed` | Country |
| Added | `local_millet_establishment_speed` | Location |
| Added | `global_millet_establishment_speed` | Country |
| Added | `local_legumes_establishment_speed` | Location |
| Added | `global_legumes_establishment_speed` | Country |
| Added | `local_potato_establishment_speed` | Location |
| Added | `global_potato_establishment_speed` | Country |
| Added | `local_livestock_establishment_speed` | Location |
| Added | `global_livestock_establishment_speed` | Country |
| Added | `local_olives_establishment_speed` | Location |
| Added | `global_olives_establishment_speed` | Country |
| Added | `local_fruit_establishment_speed` | Location |
| Added | `global_fruit_establishment_speed` | Country |
| Added | `local_beeswax_establishment_speed` | Location |
| Added | `global_beeswax_establishment_speed` | Country |
| Added | `local_slaves_goods_establishment_speed` | Location |
| Added | `global_slaves_goods_establishment_speed` | Country |
| Added | `local_camels_establishment_speed` | Location |
| Added | `global_camels_establishment_speed` | Country |
| Added | `unlocked_consulate_sea_town_right` | Country |
| Added | `allow_appoint_adelantado_mayor` | Country |
| Added | `bayt_al_mal_bureaucracy_impact_modifier` | Country |
| Added | `hisba_bureaucracy_impact_modifier` | Country |
| Added | `mazalim_court_bureaucracy_impact_modifier` | Country |
| Added | `diwan_al_insha_bureaucracy_impact_modifier` | Country |
| Added | `barid_bureaucracy_impact_modifier` | Country |
| Added | `diwan_al_hajj_bureaucracy_impact_modifier` | Country |
| Added | `diwan_al_jund_bureaucracy_impact_modifier` | Country |
| Added | `shurta_bureaucracy_impact_modifier` | Country |
| Added | `shurat_bureaucracy_impact_modifier` | Country |
| Removed | `local_food_decay_modifier` | Location |
| Removed | `monthly_complacency` | Country |
| Removed | `has_complacency_effects` | Country |
| Removed | `global_trade_through_owned_territory_efficiency` | Country |
| Removed | `complacent_decline_actions_price_cost_modifier` | Country |
| Removed | `allow_military_order_units` | Country |
| Removed | `trust_recovery` | Country |
| Removed | `trust_decay` | Country |

## On Actions
| Type | On Action | Scope |
|--|--|--|
| Added | `on_building_construction_ended` | `none/any` |
| Added | `on_character_betrothal_confirmed` | `none/any` |
| Added | `on_building_built` | `none/any` |
| Added | `on_scripted_relation_broken` | `none/any` |
| Added | `on_road_built` | `none/any` |
| Added | `on_noble_marriage` | `none/any` |
| Added | `on_character_betrothal` | `none/any` |
| Added | `on_character_changed_religion` | `none/any` |
| Added | `on_revolt_start` | `none/any` |
| Added | `on_building_construction_started` | `none/any` |
| Added | `on_ruler_death_delayed` | `country` |
| Added | `on_road_construction_started` | `none/any` |
| Added | `on_pre_location_changed_rank` | `none/any` |
| Added | `on_unconditional_surrender` | `none/any` |
| Added | `on_character_betrothal_broken` | `none/any` |
| Added | `on_game_started_after_lobby` | `none/any` |
| Added | `on_building_destroyed` | `none/any` |
| Added | `on_expedition_leader_replaced` | `none/any` |
| Added | `on_subject_subjugated` | `none/any` |
| Added | `on_scripted_relation_created` | `none/any` |
| Added | `on_character_betrothal_broken_by_death` | `none/any` |
| Added | `on_heir_changed` | `none/any` |
| Added | `on_road_construction_ended` | `none/any` |
| Added | `on_culture_group_merged` | `none/any` |
| Removed | `chinese_expedition_movement_events` | `country` |
| Removed | `on_colonial_charter_finished` | `country` |

