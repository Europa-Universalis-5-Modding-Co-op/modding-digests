#<levy_id> = {
#	unit = <unit_type>
#	size = <scriptvalue>
#   country_allow = { <triggers> } #Scope: country
#	allow = { <triggers> }	#Scope: pops
#	allow_as_crew = {
#		<triggers>	#Scope: pops
#	}
#   allowed_pop_type = <pop type> #which pop types can use this levy, can have multiple, none given means all pop types are eligible
#   allowed_culture = <culture_definition> #which culture can use this levy, can have multiple, none given means all cultures are eligible
#}

#=============================================================================
#HOW THE ENGINE PICKS A LEVY - read this before adding or editing a levy.
#=============================================================================
#
#FILE POSITION DECIDES EXACT TIES, AND NOTHING ELSE. Reordering levies changes the outcome
#only between two units of identical total combat power - see the tie-break note below.
#
#At load, CLevySetupDatabase::PostReadInit sorts every levy into exactly TWO buckets - one
#for army levies and one for navy levies - and sorts each bucket by the unit's TOTAL COMBAT
#POWER, highest first. Selection walks that sorted bucket and takes the first levy the pop
#is eligible for. Unit CATEGORY (infantry / cavalry / artillery / auxiliary) plays no part
#in the bucketing: a camelry levy competes directly against every infantry levy.
#
#TIE-BREAK. The sort is std::stable_sort under a strict greater-than comparator, so two units
#of EQUAL power keep their load order: file name order first, then declaration order within
#the file. Such a pair is decided by nothing but where it is written, and renaming or
#reordering a file silently flips which levy raises. a_moa_hunters and a_tribesmen are exactly
#this case (both 0.4693), as are a_moa_hunters and a_schiltron. If you intend a flavor levy to
#beat a generic, give it strictly more power - never rely on the tie.
#
#Therefore a levy raises only if its unit OUT-POWERS every other army unit that the same pop
#type can reach. Adding conditions never helps a levy win the pick - conditions only decide
#whether it is eligible to be considered at all.
#
#TOTAL COMBAT POWER is not combat_power alone. NAi::CArmyStrength computes it as
#  max_strength * combat_power
#    * (1 + initiative * 0.025)
#    * (1 + (flanking_ability - 1) * 0.3)
#    * (1 + morale_damage_done) * (1 - morale_damage_taken)
#    * (1 + strength_damage_done) * (1 - strength_damage_taken)
#Category defaults feed into this, so a light cavalry unit and a light infantry unit with the
#same combat_power do NOT have the same total. Do the arithmetic before assuming a levy wins.
#
#EVERY STAT LINE IS ADDITIVE, NEVER AN ASSIGNMENT. A unit's effective stat is
#  <its own accumulated value, inherited wholesale through copy_from and then added to by
#   each stat line in its own block>  +  <its category's value>
#So on a light cavalry unit (category initiative 5) that copies a parent already carrying
#initiative 5, writing "initiative = 2" yields 12, not 2. Reading these values as overrides
#will make a unit look far weaker on paper than it is.
#
#THE CHECK TO RUN whenever you add a levy or change a unit's stats:
#  1. Which pop types can use it? (allowed_pop_type - empty means ALL pop types)
#  2. Which generic levies can that pop type also reach, in EVERY age from this unit's age
#     onward? Use the reference table below.
#  3. Is this unit's total combat power higher than ALL of them, in EVERY one of those ages?
#
#If the answer is no for any age, the levy SILENTLY never raises in that age. There is no
#error, no warning, and nothing in the UI to indicate it.
#
#THE USUAL FAILURE MODE: a flavor unit copies one age's template and is never given a
#successor for later ages, while the generic ladder keeps climbing every age. The unit
#raises in its own age and is dead in every age after it. Give flavor units an age-scaled
#successor chain - a separate unit per age with its own levy, following the a_late_* /
#a_reformed_* naming convention - or accept and document that the levy is meant to stop
#working at a specific age. Do NOT reach for upgrades_to here: that field only drives
#buildable units, and has no effect on a levy. See point 4 below.
#
#POP PRESSURE IS NOT EVEN. Some pop types are far harder to win than others - see the counts
#below. A levy on tribesmen faces one competitor that never scales; the same levy on nobles
#faces eight that climb every age. Moving a levy between pop types changes how hard it is to
#raise far more than any stat edit will.
#
#COUPLING - a unit cannot be both a levy unit and buildable. levy_setup.cpp ERRORLOGs at load
#if a levy points at a buildable unit, or at a unit that is not marked levy = yes. If you
#convert a unit between levy and buildable, the unit edit, the levy creation or deletion, and
#any advance that names either of them MUST land in the same change, or the game logs errors
#on load in either order.
#
#CONVERTING A LEVY TO A BUILDABLE UNIT - four things to check, none of which errors if missed:
#
#  1. SCOPE. A levy's allow block runs in POP scope, so a culture check there tests the pop's
#     culture. A buildable unit's country_potential runs in COUNTRY scope, and its only
#     location constraint is location_potential. The same trigger line does not mean the same
#     thing in both systems.
#  2. GATES. Check all three layers - country_potential, location_potential, and any DLC gate.
#     A gate that lived on the levy disappears when the levy is deleted.
#  3. ADVANCE FIELD. An advance unlocks a levy with unlock_levy and a buildable with
#     unlock_unit. Using the wrong one is a silent no-op.
#  4. UPGRADE PATH. This is the one most easily missed. A levy needs no upgrade chain - the
#     engine re-picks the best unit in the bucket every age. A buildable is never re-picked:
#     it follows its own upgrades_to chain, and with no valid chain it keeps its starting
#     age's stats for the rest of the game. On a levy the upgrades_to field is dormant, so it
#     may be absent, stale or pointing somewhere wrong without anyone noticing. Verify the
#     chain advances one age per step and reaches a final-age unit.
#
#
#=============================================================================
#GENERIC COMPETITOR REFERENCE - the units a flavor levy must out-power
#=============================================================================
#
#A levy is GENERIC if its unit resolves (through copy_from) to a unit type with no
#is_special = yes anywhere in the chain. Army levies only (00_ through 06_); navy excluded.
#
#Generic competitor count per pop type:
#  nobles     8  (earliest Traditions - the hardest bucket in the game)
#  peasants   8
#  laborers   7
#  soldiers   6
#  burghers   4  (earliest Discovery - nothing to beat before then)
#  tribesmen  1  (Traditions only, and it NEVER scales)
#  clergy     0
#  slaves     0  (does not appear as allowed_pop_type in any land levy)
#
#NOBLES - 8 generics, Traditions -> Revolutions
#  Traditions   levy_mailed_knights      a_mailed_knights       0_knights.txt
#  Traditions   levy_noble_cavalry       a_noble_cavalry        0_knights.txt
#  Traditions   levy_chieftains          a_chieftains           0_tribal.txt
#  Renaissance  levy_plated_knights      a_plated_knights       0_knights.txt
#  Discovery    levy_cavaliers           a_cavaliers            0_knights.txt
#  Reformation  levy_late_cavaliers      a_late_cavaliers       0_knights.txt
#  Absolutism   levy_provincial_cavalry  a_provincial_cavalry   0_knights.txt
#  Revolutions  levy_gendarmerie         a_gendarmerie          0_knights.txt
#
#PEASANTS - 7 generics
#  Traditions   levy_a_villagers         a_villagers            also laborers
#  Traditions   levy_a_feudal_levy       a_feudal_levy          also laborers
#  Renaissance  levy_a_peasant_levy      a_peasant_levy         also laborers
#  Discovery    levy_a_matchlock_levy    a_matchlock_levy       also laborers/soldiers/burghers
#  Reformation  levy_a_flintlock_levy    a_flintlock_levy       also laborers/soldiers/burghers
#  Absolutism   levy_a_militiamen        a_militiamen           also laborers/soldiers/burghers
#  Revolutions  levy_conscripts          a_conscripts           also laborers/soldiers/burghers
#
#LABORERS - 7 generics, the peasants chain minus a_tribesmen
#
#SOLDIERS - 6 generics, Traditions -> Revolutions
#  Traditions   levy_a_footmen           a_footmen_levy
#  Renaissance  levy_a_men_at_arms       a_men_at_arms_levy
#  Discovery    levy_a_matchlock_levy    a_matchlock_levy
#  Reformation  levy_a_flintlock_levy    a_flintlock_levy
#  Absolutism   levy_a_militiamen        a_militiamen
#  Revolutions  levy_conscripts          a_conscripts
#
#BURGHERS - 4 generics, none before Discovery
#  Discovery    levy_a_matchlock_levy    a_matchlock_levy
#  Reformation  levy_a_flintlock_levy    a_flintlock_levy
#  Absolutism   levy_a_militiamen        a_militiamen
#  Revolutions  levy_conscripts          a_conscripts
#
#TRIBESMEN - 1 generic, and it never scales
#  Traditions   levy_tribesmen           a_tribesmen            copy_from a_age_1_traditions_light_infantry
#  a_tribesmen has no upgrades_to and no later-age variant, so it always resolves to the
#  Traditions template even in Revolutions. A tribesmen levy that beats it beats it forever.
#  Every other tribesmen-eligible levy is is_special = yes, so it is flavor competing with
#  flavor - check those by hand, they are not in this table.
#
#CLERGY / SLAVES - no generic levy exists. clergy has only is_special levies
#(levy_crusader_knights, the levy_heavy_camelry_1..6 chain). slaves is entirely unpopulated.
