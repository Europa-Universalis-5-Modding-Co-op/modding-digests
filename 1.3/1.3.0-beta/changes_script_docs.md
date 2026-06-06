# Script Documentation 1.3.0-beta
## Table of Contents
 * [Effects](#effects)
 * [Triggers](#triggers)
 * [Event Targets](#event-targets)
 * [Iterators](#iterators)
 * [On Actions](#on-actions)
 * [Modifiers](#modifiers)
## Notes
 * **Changed** means the description, scopes or anything related to the documentation for this element has changed
 * The list of iterators do **not** include generated geographic region based iterators
 * The on action scope is based on the script documentation, for more information see the `common/on_actions` directory

## Effects
| Type | Effect | Description |
|--|--|--|
| Added | `add_access_for_attackers` | adds access in the target country for all attackers in a war |
| Added | `add_access_for_defenders` | adds access in the target country for all defenders in a war |
| Added | `add_circle_satisfaction` | Add or subtract satisfaction from an imperial circle (clamped 0–100). |
| Added | `add_country_to_circle` | Add a country to an imperial circle. |
| Added | `apply_rebel_demands` | Executes the concession effect of the target rebel's demand |
| Added | `buy_goods_from_market` | A country buys goods from a target market, paying the market buy price in gold and removing the goods from the market stockpile. Usage: buy_goods_from_market = { market = \<market\> goods = \<goods\> amount = \<amount\> } |
| Added | `change_art_worth` | Adds delta to the worth override of a work of art. Cannot make a work priceless. Copies type worth first if override is 0. |
| Added | `change_creditworthiness` | Changes the creditworthiness of a country by the given amount (positive or negative) |
| Added | `clear_circle_leader` | Clear the leader of an imperial circle. The circle remains but becomes leaderless. |
| Added | `destroy_movement` | Destroys the unit from the current scope |
| Added | `hre_start_circle_formation_effect` | Start the Imperial Circle formation process for the scope IO. No-op if already active or circles are already locked. |
| Added | `join_active_chivalric_order_of` | Joins the active chivalric order of the specified country. Does nothing if the country has no active order. |
| Added | `join_chivalric_order` | Joins the specified chivalric order. Removes any existing order membership first. |
| Added | `leave_chivalric_order` | Removes the character from any chivalric order they are currently a member of. |
| Added | `lend_unit_to_country` | Lends the entire unit to a war ally as a condottieri mercenary. Usage: lend_unit_to_country = \<country scope\> |
| Added | `recall_lent_unit` | Returns a lent unit to its owner (lender). Do NOT use destroy_mercenary for lent units — that calls Dismiss() which routes subunits to the borrower. |
| Added | `redeem_bonds` | redeems the targeted government bond; country pays back face value |
| Added | `remove_country_from_circle` | Remove a country from an imperial circle. If the country was the leader, the leader is also cleared. |
| Added | `rescue_sub_unit` | Rescues a sub unit |
| Added | `sell_bonds` | issues a government bond; country receives gold and owes bond_interest monthly |
| Added | `sell_goods_to_market` | A country sells goods into a target market, receiving the sell price for its capital location in gold and adding the goods to the market stockpile. Has no effect if the country has no capital location. Usage: sell_goods_to_market = { market = \<market\> goods = \<goods\> amount = \<amount\> } |
| Added | `set_active_chivalric_order` | Unlocks the specified chivalric order for this country and refreshes the active order immediately. |
| Added | `set_art_worth` | Sets the worth override of a work of art. -1 = priceless, 0 = use type default, positive = gold value. |
| Added | `set_circle_leader` | Set the leader of an imperial circle. The country must already be a member. |
| Added | `set_province_capital` | Locks the province capital to the target location, preventing automatic reassignment. |
| Added | `set_rebel_demands` | Sets the rebel demand for this rebel, overriding the trigger-based auto-resolve. Usage: scope:my_rebel = { set_rebel_demands = my_demand_key } |
| Added | `transfer_gold_from_estate` | Country gains gold transferred from a named estate's pool; clamped to BURGHER_GRANT_MAX_FRACTION of the estate's gold |
| Changed | `end_situation` | End a situation |
| Removed | `add_mercenary_modifier` | add a modifier to a mercenary   |
| Removed | `change_mercenary_modifier_size` | Change the strength of a modifier applied to the scope mercenary   |
| Removed | `remove_mercenary_modifier` | Remove a modifier from a mercenary   |

## Triggers
| Type | Trigger | Trait | Description |
|--|--|--|--|
| Added | `all_holy_sites_owned_by_or_below_of` |  -  | Check that every holy site of the religion has its location owned by the target country, its subjects, or its subjects' subjects |
| Added | `art_is_priceless` | Boolean | Check if a work of art is priceless (cannot be bought or sold). |
| Added | `art_price` | Value | Checks the full sale price of a work of art in gold (worth * quality factor * age factor * sell value modifier). 0 if priceless. |
| Added | `art_worth` | Value | Checks the effective gold worth of a work of art. -1 if priceless. |
| Added | `attackers_have_access_in` |  -  | checks if the attacker side has access in the country in a war |
| Added | `bond_capacity` | Value | Checks the remaining bond issuance capacity of a country |
| Added | `character_is_eligible_for_active_order` |  -  | Checks if the character meets the character_eligible conditions of the active chivalric order of the given country. |
| Added | `character_is_in_order` |  -  | Checks if the character is a member of the specified chivalric order. |
| Added | `circles_are_active` | Boolean | Are Imperial Circles active in the scope international organization? |
| Added | `country_has_order` |  -  | Checks if the country's active chivalric order law references the specified order. |
| Added | `creditworthiness` | Value | Checks the effective creditworthiness (0-1 scale; 0.5 is neutral) of a country |
| Added | `cultural_influence_power` | Value | Cultural influence normalized to 0-1 range (influence / INFLUENCE_POWER_SCALE, clamped). |
| Added | `cultural_tradition_power` | Value | Cultural tradition normalized to 0-1 range (tradition / TRADITION_POWER_SCALE, clamped). |
| Added | `current_bonds` | Value | Checks how much a country has in outstanding government bond debt |
| Added | `debt_to_estates` | Value | Checks how much a country has in estate loan debt |
| Added | `defenders_have_access_in` |  -  | checks if the defender side has access in the country in a war |
| Added | `foreign_debt` | Value | Checks how much a country has in foreign bank loan debt |
| Added | `great_power_points` | Value | Checks a country's Great Power points accumulated from dominated areas |
| Added | `has_chivalric_order` | Boolean | Checks if the country has an active chivalric order (i.e. the ruler has joined one). |
| Added | `has_circle_leader` | Boolean | Does this imperial circle have a leader? |
| Added | `has_different_order_of_chivalry` |  -  | Checks if this country and the target country both have different orders. |
| Added | `has_pretender` | Boolean | Checks if a rebel has a pretender character |
| Added | `has_sellable_art` | Boolean | Check if a country has any non-priceless work of art. |
| Added | `hre_io_is_in_formation_period` | Boolean | Is the scope IO currently in the circle formation period? |
| Added | `imperial_circle_member_count` | Value | Number of members in this imperial circle. |
| Added | `imperial_circle_satisfaction` | Value | Satisfaction level (0–100) of this Imperial Circle. |
| Added | `in_same_imperial_circle` |  -  | Are the scope country and target country members of the same Imperial Circle? |
| Added | `international_organization_land_can_be_removed_by_peace_treaty` | Boolean | Return true if locations of this international organization can be removed by the 'remove location from IO' peace treaty |
| Added | `io_total_tax_base` | Value | Returns the cached sum of total tax of all members of an international organization (updated monthly) |
| Added | `is_bond` | Boolean | Checks if the loan is a government bond |
| Added | `is_condottieri` | Boolean | subunit is a lent unit (condottieri) |
| Added | `is_connected_to_through_realm` |  -  | Check if a location is connected by land/strait to another location in the same realm (top overlord and all subjects) |
| Added | `is_country_leader_of_circle` |  -  | Is the specified country the leader of this Imperial Circle? |
| Added | `is_defined_from_culture` |  -  | If a culture was originally defined as (or merged from) the target culture. |
| Added | `is_dormant_imperial_circle` | Boolean | Is this imperial circle dormant? |
| Added | `is_estate_loan` | Boolean | Checks if the loan is an estate loan (not from a banking country) |
| Added | `is_imperial_circle_leader` | Boolean | Is this country the leader of any Imperial Circle? |
| Added | `is_in_chivalric_order` | Boolean | Checks if the character is a member of any chivalric order. |
| Added | `is_leader_of_any_imperial_circle_in_io` |  -  | Is this country the leader of any Imperial Circle in the specified IO? |
| Added | `is_leader_of_imperial_circle` |  -  | Is this country the leader of the specified Imperial Circle? |
| Added | `is_lent_unit` | Boolean | Check if a mercenary is a unit lent from an ally |
| Added | `is_member_of_circle` |  -  | Is this country a member of the specified Imperial Circle? |
| Added | `is_neighbor_of_country_or_across_one_seazone` |  -  | Is the country or location a Neighbor to the specified country, or only a single seazone apart? |
| Added | `is_regional_power` | Boolean | country is a regional power |
| Added | `is_system_automated` |  -  | Checks if an automated system is active for the country. Usage: is_system_automated = credit |
| Added | `is_withering` | Boolean | Checks if a market is withering (sustained at-or-below MARKET_WITHERING_LOCATION_THRESHOLD locations with a fallback market available for most of them) |
| Added | `long_term_eco_growth` | Value | Checks the long-term (50-year) economic base growth rate of a country |
| Added | `market_location_count` | Value | Number of locations currently assigned to this market |
| Added | `mercenary_hire_cost` | Value | Cost to hire this sub unit as a mercenary |
| Added | `mercenary_maintenance_cost` | Value | Cost to maintain this sub unit as a mercenary |
| Added | `months_at_or_below_withering_threshold` | Value | How many consecutive months this market has had \<= MARKET_WITHERING_LOCATION_THRESHOLD locations |
| Added | `num_bonds` | Value | Checks if a country has a certain amount of government bonds outstanding |
| Added | `num_of_locations_with_high_conquer_desire` | Value | Gets how many locations the AI wants to conquer from the supplied country - usage: num_of_locations_with_high_conquer_desire(\<target\>) or num_of_locations_with_high_conquer_desire = { target = \<country link\> value \<operator\> \<amount\> } |
| Added | `potential_army_size` | Value | Gets the total number of armies the country has and could raise |
| Added | `potential_navy_size` | Value | Gets the total number of navies the country has and could raise |
| Added | `powerful_ally_weight` | Value | Sum of alliance_weight modifiers across all allies (Great Powers = 1.0, Regional Powers = 0.5 by default) |
| Added | `province_average_max_control` | Value | Checks the average maximum control of a province |
| Added | `short_term_eco_growth` | Value | Checks the short-term (5-year) economic base growth rate of a country |
| Added | `union_partner_weight` | Value | Sum of union_weight modifiers across all co-members (Great Powers = 1.0, Regional Powers = 0.5 by default) |
| Changed | `great_power_ranking` | Value | Country's rank among Great Powers (1 = most points) |
| Changed | `great_power_score` | Value | Checks a country's Great Power points (area-dominance score) |
| Changed | `io_total_great_power_score` | Value | Returns the cached sum of great power scores of all members of an international organization (updated monthly) |
| Changed | `io_total_military_strength` | Value | Returns the cached sum of army strengths of all members of an international organization (updated monthly) |
| Removed | `has_mercenary_modifier` |  -  | Does the scoped mercenary have a given modifier   |
| Removed | `mercenary_modifier_strength` | Value | Does the scoped mercenary have a given modifier with the compared strength. Default modifiers without any scale changes have a strength value of 1   |

## Event Targets
| Type | Event Target | Description |
|--|--|--|
| Added | `chivalric_order` | Unknown, add something in code registration |
| Added | `active_chivalric_order` | Gets the chivalric order currently active for this country. Invalid if the country has no active order. |
| Added | `joined_chivalric_order` | Gets the chivalric order this character has joined. Invalid if the character is not a member of any order. |
| Added | `circle_leader` | Unknown, add something in code registration |
| Added | `pretender` | Unknown, add something in code registration |
| Added | `mercenary` | Unknown, add something in code registration |

## Iterators
| Type | Iterator |
|--|--|
| Added | `{any\|every\|ordered\|random}_circle_member` |
| Added | `{any\|every\|ordered\|random}_country_with_chivalric_order` |
| Added | `{any\|every\|ordered\|random}_every_rented_out_mercenary` |
| Added | `{any\|every\|ordered\|random}_imperial_circle` |
| Added | `{any\|every\|ordered\|random}_imperial_circle_country_is_member_of` |
| Added | `{any\|every\|ordered\|random}_past_court_dialect` |
## On Actions
| Type | On Action | Scope |
|--|--|--|
| Added | `on_new_age_global` | `none` |
| Added | `on_estate_culture_changed` | `none` |
| Added | `on_estate_religion_changed` | `none` |

## Modifiers
### cost > efficiency
| Old | New |
| -- | -- |
| `army_reinforce_cost` | `army_reinforce_efficiency` |
| `building_upkeep_costs` | `building_upkeep_efficiency` |
| `colonial_maintenance_cost` | `colonial_maintenance_efficiency` |
| `court_spending_cost_modifier` | `court_spending_efficiency` |
| `diplomatic_annexation_cost` | `diplomatic_annexation_efficiency` |
| `diplomatic_upkeep_modifier` | `diplomatic_upkeep_efficiency` |
| `exploration_maintenance_cost` | `exploration_maintenance_efficiency` |
| `food_purchase_cost` | `food_purchase_efficiency` |
| `foreign_export_from_market_cost_modifier` | `foreign_export_from_market_efficiency` |
| `fort_maintenance_cost` | `fort_maintenance_efficiency` |
| `global_build_buildings_cost` | `global_build_buildings_efficiency` |
| `global_bureaucracy_implementation_cost_modifier` | `global_bureaucracy_implementation_efficiency` |
| `global_bureaucracy_maintenance_cost_modifier` | `global_bureaucracy_maintenance_efficiency` |
| `global_bureaucracy_removal_cost_modifier` | `global_bureaucracy_removal_efficiency` |
| `global_foreign_build_buildings_cost` | `global_foreign_build_buildings_efficiency` |
| `global_fort_build_buildings_cost` | `global_fort_build_buildings_efficiency` |
| `global_port_build_buildings_cost` | `global_port_build_buildings_efficiency` |
| `global_rural_build_buildings_cost` | `global_rural_build_buildings_efficiency` |
| `global_trade_through_owned_territory_cost_modifier` | `global_trade_through_owned_territory_efficiency` |
| `global_urban_build_buildings_cost` | `global_urban_build_buildings_efficiency` |
| `hire_for_cabinet_cost_modifier` | `hire_for_cabinet_efficiency` |
| `hostile_diplomatic_annexation_cost` | `hostile_diplomatic_annexation_efficiency` |
| `local_build_buildings_cost` | `local_build_buildings_efficiency` |
| `local_build_new_buildings_cost` | `local_build_new_buildings_efficiency` |
| `local_fort_maintenance_cost` | `local_fort_maintenance_efficiency` |
| `local_port_build_buildings_cost` | `local_port_build_buildings_efficiency` |
| `local_trade_embark_disembark_cost_modifier` | `local_trade_embark_disembark_efficiency` |
| `navy_repair_cost` | `navy_repair_efficiency` |
| `stability_cost` | `stability_cost_efficiency` |

### Additions and removals
| Type | Modifier |
| -- | -- |
| Removed | `appanage_prevented_from_call_to_war` |
| Removed | `attract_condottieri_price_cost_modifier` |
| Removed | `great_power_score` |
| Removed | `great_power_score_exempt_from_forfeit` |
| Removed | `great_power_score_modifier` |
| Removed | `has_chivalric_order` |
| Removed | `is_in_chivalric_order` |
| Removed | `peasants_allowed_weapons` |
| Added | `accepted_culture_maintenance_cost_modifier` |
| Added | `admiralty_board_bureaucracy_impact_modifier` |
| Added | `alliance_weight` |
| Added | `allow_apprenticeships_education` |
| Added | `allow_clerical_archives` |
| Added | `allow_dun_fort` |
| Added | `allow_guild_hall` |
| Added | `allow_guilds_of_florence_law` |
| Added | `allow_kulm_town_rights` |
| Added | `allow_local_noble_delegation` |
| Added | `allow_magdeburg_rights_town_rights` |
| Added | `allow_military_order_units` |
| Added | `allow_nobility_fortifications` |
| Added | `allow_noble_villa` |
| Added | `allow_nobles_recruitment_center` |
| Added | `allow_novi_fori_town_rights` |
| Added | `allow_nuremberg_rights_town_rights` |
| Added | `allow_peasants_hunting_grounds` |
| Added | `allow_peasants_training_grounds` |
| Added | `allow_theocratic_education` |
| Added | `allow_ville_franche_town_rights` |
| Added | `allow_warrior_monks_training_grounds` |
| Added | `antagonism_development_impact` |
| Added | `audit_bureau_bureaucracy_impact_modifier` |
| Added | `base_burghers_estate_power_modifier` |
| Added | `base_clergy_estate_power_modifier` |
| Added | `base_cossacks_estate_power_modifier` |
| Added | `base_crown_estate_power_modifier` |
| Added | `base_dhimmi_estate_power_modifier` |
| Added | `base_nobles_estate_power_modifier` |
| Added | `base_peasants_estate_power_modifier` |
| Added | `base_tribes_estate_power_modifier` |
| Added | `block_forums_of_thought` |
| Added | `board_of_revenue_bureaucracy_impact_modifier` |
| Added | `bond_interest` |
| Added | `bond_size_modifier` |
| Added | `building_upkeep_multiplier` |
| Added | `burghers_estate_power_from_cabinet` |
| Added | `calvinist_preachers_building_cost_modifier` |
| Added | `can_sell_bonds` |
| Added | `central_secretariat_bureaucracy_impact_modifier` |
| Added | `challenge_league_leadership_price_cost_modifier` |
| Added | `clergy_estate_power_from_cabinet` |
| Added | `colonial_office_bureaucracy_impact_modifier` |
| Added | `commissariat_bureaucracy_impact_modifier` |
| Added | `cossacks_estate_power_from_cabinet` |
| Added | `creditworthiness_bonus` |
| Added | `crown_estate_power_from_cabinet` |
| Added | `dhimmi_estate_power_from_cabinet` |
| Added | `dynastic_acquisition_preference_modifier` |
| Added | `establish_italian_administration_center_price_cost_modifier` |
| Added | `foreign_ministry_bureaucracy_impact_modifier` |
| Added | `fortify_key_location_price_cost_modifier` |
| Added | `french_subject_prevented_from_call_to_war` |
| Added | `friendly_movement_cost` |
| Added | `ghibelline_imperial_protection` |
| Added | `global_building_establishment_speed` |
| Added | `global_mills_build_buildings_efficiency` |
| Added | `global_pop_demand` |
| Added | `grand_secretariat_bureaucracy_impact_modifier` |
| Added | `high_kingship_overthrow_cost_modifier` |
| Added | `high_kingship_reclaim_land_cost_modifier` |
| Added | `high_kingship_subjugate_member_cost_modifier` |
| Added | `hostile_movement_cost` |
| Added | `imperial_censorate_bureaucracy_impact_modifier` |
| Added | `italian_league_sponsor_agenda_impact` |
| Added | `italian_league_sponsor_can_participate_in_parliament` |
| Added | `italian_league_sponsor_gold_price_cost_modifier` |
| Added | `italian_league_sponsor_manpower_price_cost_modifier` |
| Added | `local_building_establishment_reduction` |
| Added | `local_building_establishment_speed` |
| Added | `local_calvinism_movement_growth_modifier` |
| Added | `local_calvinism_movement_resistance_modifier` |
| Added | `local_lutheranism_movement_growth_modifier` |
| Added | `local_lutheranism_movement_resistance_modifier` |
| Added | `local_may_build_north_american_units` |
| Added | `local_mills_build_buildings_efficiency` |
| Added | `local_pop_demand` |
| Added | `lutheran_preachers_building_cost_modifier` |
| Added | `max_bonds` |
| Added | `max_bonds_modifier` |
| Added | `merge_colonies_price_cost_modifier` |
| Added | `monthly_creditworthiness_change` |
| Added | `national_calvinism_movement_growth_modifier` |
| Added | `national_calvinism_movement_resistance_modifier` |
| Added | `national_lutheranism_movement_growth_modifier` |
| Added | `national_lutheranism_movement_resistance_modifier` |
| Added | `negotiate_rebels_buy_off_price_cost_modifier` |
| Added | `nobles_estate_power_from_cabinet` |
| Added | `num_italian_administrations` |
| Added | `ordnance_board_bureaucracy_impact_modifier` |
| Added | `peasants_estate_power_from_cabinet` |
| Added | `privy_council_bureaucracy_impact_modifier` |
| Added | `profess_trust_price_cost_modifier` |
| Added | `request_divorce_price_cost_modifier` |
| Added | `request_work_of_art_purchase_cost_modifier` |
| Added | `sell_work_of_art_cost_modifier` |
| Added | `set_province_capital_cost_modifier` |
| Added | `six_boards_bureaucracy_impact_modifier` |
| Added | `sponsor_the_reformation_cost_modifier` |
| Added | `tolerated_culture_maintenance_cost_modifier` |
| Added | `trade_commission_bureaucracy_impact_modifier` |
| Added | `tribes_estate_power_from_cabinet` |
| Added | `twilight_of_the_tsardom_disaster_actions_price_cost_modifier` |
| Added | `unintegrated_land_expansion_penalty_modifier` |
| Added | `union_weight` |
| Added | `war_council_bureaucracy_impact_modifier` |
| Added | `win_war_chance_lower_limit` |
| Added | `work_of_art_sell_value_modifier` |