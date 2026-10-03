# Release 1.4.0 - Beta
## Breaking Changes
- Removed complacency mechanic
## Type Documentation
Selected changes and additions
### Building types
 - Added `ai_construct_weight` and `ai_destroy_weight` script values
### Country interactions
 - Added `terminate_pending_offers_if` trigger and `potential_diplomatic_capacity_used` script value
 - Changed GUI widget script to use `scripted_action_tooltip` with specialized parameters
### Disasters
 - Added `ends_on_regime_change` boolean
### Expedition types
 - New type
### Generic actions
 - Added `ai_prerequisite_after_potential` trigger, `goods_demand` goods list, and `price_location` scripted location
 - Changed GUI widget script to use `scripted_action_tooltip` with specialized parameters
### Industry types
 - New type
### International organizations
 - Added `embargo`, `assists_in_rebellions`, and `assists_in_civil_wars` booleans
### Religious order types
 - New type
### Resolutions
 - Added `validate_vote_trigger` trigger and `ai_vote_weight` as alternative name for `ai_will_do` script value
 - Renamed `ai_will_select` script value to `ai_will_propose`
 - Changed GUI widget script to use `scripted_action_tooltip` with specialized parameters
### Road types
 - Added `ai_construct_weight` script value
 - Added `on_construction_started`, `on_construction_ended`, and `on_built` effect blocks
### Scripted relations
 - Added `dangerous_relation`, `can_get_without_buying`, `always_shown_when_unaffordable`, `diplomatic_map_stripe`, and `use_with_enemies` booleans
 - Clarified effect of `wants_to_keep` script value when negative
### Situations
 - Added `warning_string_key` localization and `variables` list
### Subject types
 - Removed `overlord_protects_external`, `overlord_protects_other_subjects`, and `counts_as_external` booleans
 - Added `ai_biases` script value
### Unit families
 - New type

## Data Type Documentation 
 * [Table of Contents](changes_data_types.md#table-of-contents)
 * [Types](changes_data_types.md#types)
 * [Global Functions](changes_data_types.md#global-functions)
 * [Global Promotes](changes_data_types.md#global-promotes)
## Script Documentation 
 * [Table of Contents](changes_script_docs.md#table-of-contents)
 * [Scopes](changes_script_docs.md#scopes)
 * [Effects](changes_script_docs.md#effects)
 * [Triggers](changes_script_docs.md#triggers)
 * [Event Targets](changes_script_docs.md#event-targets)
 * [Iterators](changes_script_docs.md#iterators)
 * [Modifiers](changes_script_docs.md#modifiers)
 * [On Actions](changes_script_docs.md#on-actions)

## File Changes
File changes can be found below.

**Link:** [File Changes](./changes_files.md)
## Digest Repository
- https://github.com/Europa-Universalis-5-Modding-Co-op/modding-digests