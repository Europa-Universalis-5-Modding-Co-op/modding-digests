# Scripted relations
# These are relations that can be toggled on or off between countries through diplo actions
#
#<name> = {
#	type = <diplomacy/subject> defines if the relation type is something you can have with every country or only with subjects
#	relation_type = <oneway/mutual> determines if the relationship is a giving/receiving kind or if partners are mutual in the relationship
#   uses_diplo_capacity = <none/mutual/giving/receiving> whether this relation uses a diplo relation slot
#   diplomatic_capacity_cost = <scriptvalue>
#	block_when_at_war = <yes/no> whether we can or can't use this relation while at war
#	break_on_war = <yes/no> ends the relationship if either sides ends up in a war against the other side
#   break_on_becoming_subject = <yes/no> ends the relationship if one side becomes a subject of another country
#   break_on_not_spying = <yes/no> ends the relationship if the perpetrator stops building a spy network in the target country, including if their spy is discovered
#	annulled_by_peace_treaty = <yes/no> does this relationship get cancelled when an "annul treaties" peace treaty between the two countries is executed
#	disallow_war = <yes/no> does this forbid declarations of war between the two countries
#	embargo = <yes/no> does this relationship cause an embargo between the two countries
#   military_access = <yes/no> does this relationship give military access between the two countries (if it's mutual, either way; if it's one way, then the receiver gets the rights)
#   fleet_basing_rights = <yes/no> does this relationship give fleet basing rights between the two countries (if it's mutual, either way; if it's one way, then the receiver gets the rights)
#   food_access = <yes/no> does this relationship give food access between the two countries (if it's mutual, either way; if it's one way, then the receiver gets the rights)
#	is_exempt_from_sound_toll = <yes/no> does this relationship give an exemption from sound tolls
#	is_exempt_from_isolation = <yes/no> does this relationship give exemptions from being isolated from the trade network
#	block_building = <yes/no> does this block the receiver (one way)/both parties (mutual) from building foreign buildings in the other's territory
#	skip_diplomat_for_cancel = <yes/no> do we skip diplomat travel time when cancelling/breaking
#   lifts_fog_of_war = <yes/no> does this relation lift the fog of war in their territory
#	called_in_defensively = <none/mutual/giving/receiving> are calls to arms sent when one party gets war declared on them
#	called_in_offensively = <none/mutual/giving/receiving> are calls to arms sent when one party declares war
#   lifts_trade_protection = <yes/no> is market trade protectionism lifted between the countries
#	trade_to_first = <script value> increases the attraction of the first country's markets in locations belonging to the second country
#	trade_to_second = <script value> increases the attraction of the second country's markets in locations belonging to the first country
#	gold_to_first = <script value> amount of gold that the second country gives the first per month
#	gold_to_second = <script value> amount of gold that the first country gives the second per month
#	favors_to_first = <script value> amount of favors that the second country gives the first per month
#	favors_to_second = <script value> amount of favors that the first country gives the second per month
#	institution_spread_to_first = <script value> amount of institution spread that the second country sends to the first country's capital per month
#	institution_spread_to_second = <script value>amount of institution spread that the first country sends to the second country's capital per month
#	diplomatic_cost = <price> cost to create this relation
#	war_declaration_cost = <price> cost to declare war between the two countries
#	buy_price = <price> cost to buy the relation (if not specified, you can't buy it)
#	monthly_ongoing_price_first_country = <price> monthly cost to maintain the relation for the first country (applies to both if mutual)
#	monthly_ongoing_price_second_country = <price> monthly cost to maintain the relation for the second country in a one way relation
#
#	sound = "<sound gfx>" sound that should play once this relationship is established
#	mutual_color = <color definition> for the diplomacy map mode
#	giving_color = <color definition> for the diplomacy map mode
#	receiving_color = <color definition> for the diplomacy map mode
#
#	visible = <trigger> should the relationship to be visible in the first place
#   offer_visible = <yes/no> is offering this relationship available
#   request_visible = <yes/no> is requesting this relationship available
#   cancel_visible = <yes/no> is cancelling this relationship available
#   break_visible = <yes/no> is breaking this relationship available
#	offer_enabled = <triggers> can we offer to establish this relationship (i.e. offer to give the one way relationship) (mutual counts here)
#	request_enabled = <triggers> can we request the relationship (i.e. request to receive the one way relationship)
#	cancel_enabled = <triggers> can we cancel a relationship that is either mutual or is one way that we are giving
#	break_enabled = <triggers> can we break a one way relationship we are receiving
#	will_expire_trigger = <triggers> criteria for this relationship auto-expiring
#
#	wants_to_give = <ai evaluation> - use this one for both mutual and one way relations. Calculation when a request is being evaluated.
#	wants_to_receive = <ai evaluation> - one way relations only. Calculation when an offer is being evaluated.
#	wants_to_give_diplo_chance = <diplo evaluation> - only use this one for mutual and one way relations. Calculation when a request is being evaluated.
#	wants_to_receive_diplo_chance = <diplo evaluation> - one way relations only. Calculation when an offer is being evaluated.
#   wants_to_keep = <ai evaluation> - use this for both mutual and one way relations. If evaluation results in values below or equal 0 ai will try to cancel/break relation
#   wants_to_keep_diplo_chance = <diplo evaluation> - use this for both mutual and one way relations.
#
#	offer_effect = <effects> what happens when an offer is accepted
#	request_effect = <effects> what happens when a request is accepted
#	cancel_effect = <effects> what happens when a relation is cancelled
#	break_effect = <effects> what happens when a relation is broken
#	offer_declined_effect = <effects> what happens when an offer for a relation is declined
#	request_declined_effect = <effects> what happens when an request for a relation is declined
#   expire_effect = <effects> what happens when a relation expires
#
#Ongoing actions - this meta data is used for when you want the relation to show in the ongoing actions area of the diplomacy panel
#Also add a string with _ongoing_tooltip suffix to show when it's hovered over
#   is_ongoing = <yes/no> makes it show up in the ongoing diplomacy area
#   texture_file = <string> texture to use for the icon in the ongoing diplomacy area
#   concept - <string> concept to use in the tooltip (like "annex" or "country")
#	progress = <script value> returns a number between 0 and 100 for how far through the process the ongoing action is (scope:first and scope:second are the countries in the relation)
#}
#
# Modifiers automatically apply for countries that have a scripted relation. These can be specified as follows:
# <key>: modifier added when having a mutual relation
# giving_<key>: modifier added when giving the one-way relation
# receiving_<key>: modifier added when receiving the one-way relation
#
# You can have biases auto-apply for when the relation is operational between two countries.
# opinion_<key>: opinion of a country added when having a mutual relation with them
# opinion_giving_<key>: opinion of a country added when giving the one-way relation to them
# opinion_receiving_<key>: opinion of a country added when receiving the one-way relation from them
# opinion_decline_<key>: opinion of a country added when the relation was declined
# trust_<key>: trust of a country added when having a mutual relation with them
# trust_giving_<key>: trust of a country added when giving the one-way relation to them
# trust_receiving_<key>: trust of a country added when receiving the one-way relation from them
# trust_decline_<key>: trust of a country added when the relation was declined

#################################
# Values used for diplo chances #
#################################
# at_war
# recipient_at_war
# actor_at_war
# recipient_civil_war
# actor_civil_war
# multiple_offensive_wars
# actor_is_rival
# recipient_is_rival
# same_religion
# different_religion
# same_culture
# same_court_language
# same_common_language
# different_culture
# diplomatic_reputation
# culture_war
# opinion
# warscore
# peaceoffer
# peaceoffer_most_of_wanted
# months_at_war
# planning_demise
# conflicting_interests
# max_relations
# actor_max_relations
# capital_distance
# yesman
# defeat
# victory
# has_border
# same_international_organization
# giving_defensive_support
# receiving_defensive_support
# base
# giving_them_access
# in_debt
# cost
# claim
# current_strength
# potential_strength
# relative_strength
# capital
# location_value
# interesting
# vital
# avoided
# stability
# positive_stability
# negative_stability
# war_exhaustion
# low_manpower
# disloyal_subject
# no_action
# separate_peace
# junior_to
# price
# desperation
# war_balance
# war_goal
# making_gains
# on_retreat
# tutorial
# target_opinion
# lacks_border
# another_war
# fighting_together
# border_distance
# province_distance
# revolter
# rank
# rank_difference
# common_threat
# competing_power
# recipient_at_peace
# actor_at_peace
# best_possible_offer
# substantial_land_lost
# last_major_battle
# few_relations
# no_access
# positive_opinion
# negative_opinion
# allied_to_enemy
# enforced_demand
# ai_setting
# has_truce
# has_truce_with_target
# overlord
# my_proposal
# heir
# interest_rate_too_high
# good_interest_rate
# existing_loans_from_country
# too_many_loans
# need_loan
# loan_is_insignificant
# loan_ends_too_soon
# loan_ends_too_late
# using_favors
# unbalanced_favors
# trust_in_actor
# trust_in_recipient
# not_1_trust
# not_5_trust
# not_10_trust
# not_15_trust
# not_20_trust
# same_government_type
# different_government_type
# estates_like
# estates_dislike
# culture_view
# religion_view
# royal_ties
# call_for_peace
# war_enthusiam
# want_more
# too_much_antagonism number of countries that will go over the antagonism limit the country is willing to take
# want_something_else
# tax_base
# promised_land
# demands_made
# belongs_to_international_organization
# different_religion_group
# conquer_desire
# produced_goods
# price_percentage_of_treasury_funds
# antagonism