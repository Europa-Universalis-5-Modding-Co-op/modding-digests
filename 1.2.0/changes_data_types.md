# Data Type Documentation 1.2.0
## Table of Contents
* [Types](#types)
* [Global Promotes](#global-promotes)
## Notes
This is just a very basic overview of added and removed data types.

Changed elements are **not** mentioned here.
## Types
| Type    | Data Type                                                   |
| ------- | ----------------------------------------------------------- |
| Added   | `Bureaucracy`                                               |
| Added   | `BureaucracyType`                                           |
| Added   | `Movement`                                                  |
| Added   | `MovementDefinition`                                        |
| Added   | `Omen`                                                      |
| Added   | `TownRights`                                                |
| Added   | `TownRightsType`                                            |
| Added   | `AiPersonality`                                             |
| Added   | `AlertAnnexingStalledLowOpinion`                            |
| Added   | `AlertCanComposeStrategikon`                                |
| Added   | `AlertCanUseHreEmperorAction`                               |
| Added   | `AlertObjectiveGroupMissingTransportNavy`                   |
| Added   | `AreaPreference`                                            |
| Added   | `BureaucraciesLateralView`                                  |
| Added   | `Bureaucracy`                                               |
| Added   | `BureaucracyItem`                                           |
| Added   | `BureaucracyType`                                           |
| Added   | `CPdxStringView`                                            |
| Added   | `CountryDHEView`                                            |
| Added   | `CultureData`                                               |
| Added   | `DHEEventEntry`                                             |
| Added   | `GameLobbyDLCView`                                          |
| Added   | `HreHeaderActionItem`                                       |
| Added   | `ImperialDietInSession`                                     |
| Added   | `IoSubheaderSelectMenu`                                     |
| Added   | `LocationGoodItem`                                          |
| Added   | `LocationSupplyWrap`                                        |
| Added   | `LocationUpKeepBuildingItem`                                |
| Added   | `LocationUpkeepWrap`                                        |
| Added   | `MapModeSlot`                                               |
| Added   | `MarketPopNeedsWrap`                                        |
| Added   | `MarketValueContributionItem`                               |
| Added   | `MarketValuePieChartWidget`                                 |
| Added   | `MilitaryLedger`                                            |
| Added   | `MilitaryLedgerItem`                                        |
| Added   | `Movement`                                                  |
| Added   | `MovementDefinition`                                        |
| Added   | `MovementModifierWrap`                                      |
| Added   | `Omen`                                                      |
| Added   | `PeopleMovementItem`                                        |
| Added   | `PopEstatePerLocationPowerWrap`                             |
| Added   | `ProvinceLevySizeWrap`                                      |
| Added   | `QuickMovements`                                            |
| Added   | `QuickOrderItem`                                            |
| Added   | `RegimentItem`                                              |
| Added   | `RegimentsView`                                             |
| Added   | `RiskStarvingProvincesMarketEntry`                          |
| Added   | `SPopNeedsBreakdownWrapper`                                 |
| Added   | `ShipItem`                                                  |
| Added   | `ShipsView`                                                 |
| Added   | `SocietalValuesSelectMenu`                                  |
| Added   | `Spreadable`                                                |
| Added   | `StarvingProvincesMarketEntry`                              |
| Added   | `StringViewPair`                                            |
| Added   | `TableRow`                                                  |
| Added   | `TableRowList`                                              |
| Added   | `TownRights`                                                |
| Added   | `TownRightsItem`                                            |
| Added   | `TownRightsLateralView`                                     |
| Added   | `TownRightsType`                                            |
| Added   | `TradeConnectionWrap`                                       |
| Added   | `TradeOrderItem`                                            |
| Added   | `UniqueContentTypeCategory`                                 |
| Added   | `UnitDefCostWrap`                                           |
| Added   | `UnitMaintenanceWrap`                                       |
| Added   | `UnitRepairWrap`                                            |
 
## Global Promotes
| Type    | Promote                                                     | Return Type              |
| ------- | ----------------------------------------------------------- | ------------------------ |
| Added   | `AI_PERSONALITY`                                            | `AiPersonality`          |
| Added   | `AREA_PREFERENCE`                                           | `AreaPreference`         |
| Added   | `ActiveMapModeForSlot( Arg0 )`                              | `MapMode`                |
| Added   | `BUREAUCRACY`                                               | `Bureaucracy`            |
| Added   | `BUREAUCRACY_TYPE`                                          | `BureaucracyType`        |
| Added   | `GetGameDLCFromKey( Arg0 )`                                 | `GameDLC`                |
| Added   | `GetLocationByKey( Arg0 )`                                  | `Location`               |
| Added   | `GetQuickMovements( Arg0 )`                                 | `QuickMovements`         |
| Added   | `GoodsDetailsModeGetView`                                   | `GoodsDetailsLateralView`|
| Added   | `MOVEMENT`                                                  | `Movement`               |
| Added   | `MOVEMENT_DEFINITION`                                       | `MovementDefinition`     |
| Added   | `OMEN`                                                      | `Omen`                   |
| Added   | `StringToRequirementsWithDLC( Arg0, Arg1 )`                 | `RequirementsList`       |
| Added   | `StringToTableRowList( Arg0 )`                              | `TableRowList`           |
| Added   | `TARGET_AI_PERSONALITY`                                     | `AiPersonality`          |
| Added   | `TARGET_AREA_PREFERENCE`                                    | `AreaPreference`         |
| Added   | `TARGET_BUREAUCRACY`                                        | `Bureaucracy`            |
| Added   | `TARGET_BUREAUCRACY_TYPE`                                   | `BureaucracyType`        |
| Added   | `TARGET_MOVEMENT`                                           | `Movement`               |
| Added   | `TARGET_MOVEMENT_DEFINITION`                                | `MovementDefinition`     |
| Added   | `TARGET_OMEN`                                               | `Omen`                   |
| Added   | `TARGET_TOWN_RIGHTS`                                        | `TownRights`             |
| Added   | `TARGET_TOWN_RIGHTS_TYPE`                                   | `TownRightsType`         |
| Added   | `TOWN_RIGHTS`                                               | `TownRights`             |
| Added   | `TOWN_RIGHTS_TYPE`                                          | `TownRightsType`         |
| Added   | `ActiveMapModeForSlot( Arg0 )`                              | `[unregistered]`         |
| Added   | `CycleSlot( Arg0 )`                                         | `void`                   |
| Added   | `GetAiConquerDesireDesc( Arg0 )`                            | `CString`                |
| Added   | `GetAiDispositionDescForKey( Arg0 )`                        | `CString`                |
| Added   | `GetAiDispositionIcon( Arg0 )`                              | `[unregistered]`         |
| Added   | `GetAiDispositionIconForKey( Arg0 )`                        | `[unregistered]`         |
| Added   | `GetAiDispositionNameForKey( Arg0 )`                        | `CString`                |
| Added   | `GetAiPersonalityIcon( Arg0 )`                              | `[unregistered]`         |
| Added   | `GetAllMovements`                                           | `[unregistered]`         |
| Added   | `GetBureaucracyIcon( Arg0 )`                                | `[unregistered]`         |
| Added   | `GetConceptTexture_StringView( Arg0 )`                      | `[unregistered]`         |
| Added   | `GetCountryCategorySubunitsTooltip( Arg0 )`                 | `CString`                |
| Added   | `GetCreateMarketInLocationPrice( Arg0 )`                    | `CString`                |
| Added   | `GetDHETooltip( Arg0 )`                                     | `CString`                |
| Added   | `GetEmptyGodIcon( Arg0 )`                                   | `[unregistered]`         |
| Added   | `GetFullBodyGodIcon( Arg0 )`                                | `[unregistered]`         |
| Added   | `GetGameContentDLCs`                                        | `[unregistered]`         |
| Added   | `GetGameDLCFromKey( Arg0 )`                                 | `[unregistered]`         |
| Added   | `GetGraphicalCultureTextureForLocationPopType( Arg0, Arg1 )`| `[unregistered]`         |
| Added   | `GetKeepGamePausedTooltip`                                  | `CString`                |
| Added   | `GetLevySetupCultureText( Arg0 )`                           | `CString`                |
| Added   | `GetLevySetupLabel( Arg0 )`                                 | `CString`                |
| Added   | `GetMapModeMenuPinTooltip`                                  | `CString`                |
| Added   | `GetMapModesSlots`                                          | `[unregistered]`         |
| Added   | `GetMovementDefinitionIcon( Arg0 )`                         | `[unregistered]`         |
| Added   | `GetMovementDefinitions`                                    | `[unregistered]`         |
| Added   | `GetOmenIcon( Arg0 )`                                       | `[unregistered]`         |
| Added   | `GetOverallPowerRatio( Arg0, Arg1 )`                        | `CFixedPoint`            |
| Added   | `GetUnEmployedPopTypeFromLocation( Arg0, Arg1 )`            | `CString`                |
| Added   | `GetUnEmployedPopTypeFromLocationValue( Arg0, Arg1 )`       | `CFixedPoint`            |
| Added   | `GetUnitsCategoryTooltip( Arg0, Arg1, Arg2, Arg3 )`         | `CString`                |
| Added   | `GetUpgradeSubUnitName( Arg0 )`                             | `CString`                |
| Added   | `GetValidLeviesForCategoryTooltip( Arg0 )`                  | `CString`                |
| Added   | `GetWealthReachInfo( Arg0, Arg1 )`                          | `CString`                |
| Added   | `GrantLocationTownRights( Arg0 )`                           | `void`                   |
| Added   | `GrantTownRights`                                           | `void`                   |
| Added   | `HasAnyVisibleMovementDefinitions`                          | `bool`                   |
| Added   | `HasDHEEvents( Arg0 )`                                      | `bool`                   |
| Added   | `HasLevySetupCultureRestrictions( Arg0 )`                   | `bool`                   |
| Added   | `HasWealthThreshold( Arg0 )`                                | `bool`                   |
| Added   | `IsCountryPlayable( Arg0 )`                                 | `bool`                   |
| Added   | `IsDelayStartLobbyGame`                                     | `bool`                   |
| Added   | `IsGameSystemPaused`                                        | `bool`                   |
| Added   | `IsGameUserPaused`                                          | `bool`                   |
| Added   | `IsInmersionModeDisabled`                                   | `bool`                   |
| Added   | `IsMapModeMenuPinned`                                       | `bool`                   |
| Added   | `IsRenamingLocationsAllowed`                                | `bool`                   |
| Added   | `IsUTF8StringNotEmpty( Arg0 )`                              | `bool`                   |
| Added   | `MPChatHasExtraWhispers`                                    | `bool`                   |
| Added   | `MPChatLastWhisperMessage`                                  | `CString`                |
| Added   | `MPChatLastWhisperSender`                                   | `CString`                |
| Added   | `MPChatNewWhisper`                                          | `bool`                   |
| Added   | `MPChatUnreadWhisperCount`                                  | `int32`                  |
| Added   | `OpenImperialDietView`                                      | `void`                   |
| Added   | `OpenLateralViewWithFilterNoClear( Arg0, Arg1 )`            | `void`                   |
| Added   | `OpenTechnologyViewAndPanToAdvance( Arg0 )`                 | `void`                   |
| Added   | `OpenTechnologyViewAndPanToAdvanceDefinition( Arg0 )`       | `void`                   |
| Added   | `PlayerHasBureaucracies`                                    | `bool`                   |
| Added   | `SelectTownRights`                                          | `void`                   |
| Added   | `SetTableRowListFromTextContext( Arg0 )`                    | `void`                   |
| Added   | `ShowBuildingCategoryName( Arg0 )`                          | `CString`                |
| Added   | `ShowBuildingNameWithNoTooltip( Arg0 )`                     | `CString`                |
| Added   | `ShowBureaucracyTypeName( Arg0 )`                           | `CString`                |
| Added   | `ShowBureaucracyTypeNameWithNoTooltip( Arg0 )`              | `CString`                |
| Added   | `ShowDHEHistoryForCountry( Arg0 )`                          | `void`                   |
| Added   | `ShowDLCView( Arg0 )`                                       | `void`                   |
| Added   | `ShowGrantLocationTownRights( Arg0 )`                       | `bool`                   |
| Added   | `ShowGrantTownRights`                                       | `bool`                   |
| Added   | `ShowMovementDefinitionName( Arg0 )`                        | `CString`                |
| Added   | `ShowMovementDefinitionNameWithNoTooltip( Arg0 )`           | `CString`                |
| Added   | `ShowOmenName( Arg0 )`                                      | `CString`                |
| Added   | `ShowOmenNameWithNoTooltip( Arg0 )`                         | `CString`                |
| Added   | `ShowOnlyIconModifierEffect( Arg0 )`                        | `CString`                |
| Added   | `ShowTownRightsName( Arg0 )`                                | `CString`                |
| Added   | `ShowTownRightsNameWithNoTooltip( Arg0 )`                   | `CString`                |
| Added   | `ShowUnitMilitaryObjectiveGroup( Arg0 )`                    | `void`                   |
| Added   | `ShowValues( Arg0 )`                                        | `CString`                |
| Added   | `SlotFromIndex( Arg0 )`                                     | `int32`                  |
| Added   | `SlotNameFromIndex( Arg0 )`                                 | `CString`                |
| Added   | `ToggleAutoMinting`                                         | `void`                   |
| Added   | `ToggleMapModeMenuPin`                                      | `void`                   |
| Added   | `TriggerMusicPlayerNext`                                    | `void`                   |
| Added   | `ai_disposition`                                            | `[unregistered]`         |
| Added   | `ai_disposition_icon`                                       | `[unregistered]`         |
| Added   | `ai_disposition_with_icon`                                  | `[unregistered]`         |
| Added   | `ai_dispositions`                                           | `[unregistered]`         |
| Added   | `ai_dispositions_icon`                                      | `[unregistered]`         |
| Added   | `ai_dispositions_with_icon`                                 | `[unregistered]`         |
| Added   | `ai_personalities`                                          | `[unregistered]`         |
| Added   | `ai_personalities_icon`                                     | `[unregistered]`         |
| Added   | `ai_personalities_with_icon`                                | `[unregistered]`         |
| Added   | `ai_personality`                                            | `[unregistered]`         |
| Added   | `ai_personality_icon`                                       | `[unregistered]`         |
| Added   | `ai_personality_with_icon`                                  | `[unregistered]`         |
| Added   | `bureaucracies`                                             | `[unregistered]`         |
| Added   | `bureaucracies_icon`                                        | `[unregistered]`         |
| Added   | `bureaucracies_with_icon`                                   | `[unregistered]`         |
| Added   | `bureaucracy`                                               | `[unregistered]`         |
| Added   | `bureaucracy_icon`                                          | `[unregistered]`         |
| Added   | `bureaucracy_maintenance`                                   | `[unregistered]`         |
| Added   | `bureaucracy_maintenance_short`                             | `[unregistered]`         |
| Added   | `bureaucracy_with_icon`                                     | `[unregistered]`         |
| Added   | `cabinet_trait`                                             | `[unregistered]`         |
| Added   | `cabinet_trait_icon`                                        | `[unregistered]`         |
| Added   | `cabinet_trait_with_icon`                                   | `[unregistered]`         |
| Added   | `cabinet_traits`                                            | `[unregistered]`         |
| Added   | `cabinet_traits_icon`                                       | `[unregistered]`         |
| Added   | `cabinet_traits_with_icon`                                  | `[unregistered]`         |
| Added   | `country_disposition`                                       | `[unregistered]`         |
| Added   | `country_disposition_icon`                                  | `[unregistered]`         |
| Added   | `country_disposition_with_icon`                             | `[unregistered]`         |
| Added   | `country_dispositions`                                      | `[unregistered]`         |
| Added   | `country_dispositions_icon`                                 | `[unregistered]`         |
| Added   | `country_dispositions_with_icon`                            | `[unregistered]`         |
| Added   | `country_personalities`                                     | `[unregistered]`         |
| Added   | `country_personalities_icon`                                | `[unregistered]`         |
| Added   | `country_personalities_with_icon`                           | `[unregistered]`         |
| Added   | `country_personality`                                       | `[unregistered]`         |
| Added   | `country_personality_icon`                                  | `[unregistered]`         |
| Added   | `country_personality_with_icon`                             | `[unregistered]`         |
| Added   | `divine_emperors`                                           | `[unregistered]`         |
| Added   | `divine_emperors_icon`                                      | `[unregistered]`         |
| Added   | `divine_emperors_with_icon`                                 | `[unregistered]`         |
| Added   | `divorce`                                                   | `[unregistered]`         |
| Added   | `divorce_icon`                                              | `[unregistered]`         |
| Added   | `divorce_with_icon`                                         | `[unregistered]`         |
| Added   | `divorced`                                                  | `[unregistered]`         |
| Added   | `divorced_icon`                                             | `[unregistered]`         |
| Added   | `divorced_with_icon`                                        | `[unregistered]`         |
| Added   | `entrenched`                                                | `[unregistered]`         |
| Added   | `entrenched_icon`                                           | `[unregistered]`         |
| Added   | `entrenched_with_icon`                                      | `[unregistered]`         |
| Added   | `entrenchment`                                              | `[unregistered]`         |
| Added   | `entrenchment_icon`                                         | `[unregistered]`         |
| Added   | `entrenchment_with_icon`                                    | `[unregistered]`         |
| Added   | `estate_building`                                           | `[unregistered]`         |
| Added   | `estate_building_icon`                                      | `[unregistered]`         |
| Added   | `estate_building_with_icon`                                 | `[unregistered]`         |
| Added   | `estate_buildings`                                          | `[unregistered]`         |
| Added   | `estate_buildings_icon`                                     | `[unregistered]`         |
| Added   | `estate_buildings_with_icon`                                | `[unregistered]`         |
| Added   | `export_efficiency`                                         | `[unregistered]`         |
| Added   | `export_efficiency_icon`                                    | `[unregistered]`         |
| Added   | `export_efficiency_with_icon`                               | `[unregistered]`         |
| Added   | `god_emperors`                                              | `[unregistered]`         |
| Added   | `god_emperors_icon`                                         | `[unregistered]`         |
| Added   | `god_emperors_with_icon`                                    | `[unregistered]`         |
| Added   | `gurus`                                                     | `[unregistered]`         |
| Added   | `gurus_icon`                                                | `[unregistered]`         |
| Added   | `gurus_with_icon`                                           | `[unregistered]`         |
| Added   | `health_trait`                                              | `[unregistered]`         |
| Added   | `health_trait_icon`                                         | `[unregistered]`         |
| Added   | `health_trait_short`                                        | `[unregistered]`         |
| Added   | `health_trait_short_icon`                                   | `[unregistered]`         |
| Added   | `health_trait_short_with_icon`                              | `[unregistered]`         |
| Added   | `health_trait_with_icon`                                    | `[unregistered]`         |
| Added   | `health_traits`                                             | `[unregistered]`         |
| Added   | `health_traits_icon`                                        | `[unregistered]`         |
| Added   | `health_traits_with_icon`                                   | `[unregistered]`         |
| Added   | `heroes`                                                    | `[unregistered]`         |
| Added   | `heroes_icon`                                               | `[unregistered]`         |
| Added   | `heroes_with_icon`                                          | `[unregistered]`         |
| Added   | `import_efficiency`                                         | `[unregistered]`         |
| Added   | `import_efficiency_icon`                                    | `[unregistered]`         |
| Added   | `import_efficiency_with_icon`                               | `[unregistered]`         |
| Added   | `map_mode_slot`                                             | `[unregistered]`         |
| Added   | `map_mode_slot_icon`                                        | `[unregistered]`         |
| Added   | `map_mode_slot_with_icon`                                   | `[unregistered]`         |
| Added   | `map_mode_slots`                                            | `[unregistered]`         |
| Added   | `map_mode_slots_icon`                                       | `[unregistered]`         |
| Added   | `map_mode_slots_with_icon`                                  | `[unregistered]`         |
| Added   | `movement`                                                  | `[unregistered]`         |
| Added   | `movement_definition`                                       | `[unregistered]`         |
| Added   | `movement_definitions`                                      | `[unregistered]`         |
| Added   | `movement_icon`                                             | `[unregistered]`         |
| Added   | `movement_modifier`                                         | `[unregistered]`         |
| Added   | `movement_modifier_icon`                                    | `[unregistered]`         |
| Added   | `movement_modifier_with_icon`                               | `[unregistered]`         |
| Added   | `movement_modifiers`                                        | `[unregistered]`         |
| Added   | `movement_modifiers_icon`                                   | `[unregistered]`         |
| Added   | `movement_modifiers_with_icon`                              | `[unregistered]`         |
| Added   | `movement_with_icon`                                        | `[unregistered]`         |
| Added   | `movements`                                                 | `[unregistered]`         |
| Added   | `movements_icon`                                            | `[unregistered]`         |
| Added   | `movements_with_icon`                                       | `[unregistered]`         |
| Added   | `omen`                                                      | `[unregistered]`         |
| Added   | `omen_icon`                                                 | `[unregistered]`         |
| Added   | `omen_with_icon`                                            | `[unregistered]`         |
| Added   | `omens`                                                     | `[unregistered]`         |
| Added   | `omens_icon`                                                | `[unregistered]`         |
| Added   | `omens_with_icon`                                           | `[unregistered]`         |
| Added   | `pentarchy`                                                 | `[unregistered]`         |
| Added   | `pentarchy_icon`                                            | `[unregistered]`         |
| Added   | `pentarchy_with_icon`                                       | `[unregistered]`         |
| Added   | `selling_efficiency`                                        | `[unregistered]`         |
| Added   | `selling_efficiency_icon`                                   | `[unregistered]`         |
| Added   | `selling_efficiency_with_icon`                              | `[unregistered]`         |
| Added   | `subject_territory_connectivity`                            | `[unregistered]`         |
| Added   | `subject_territory_connectivity_icon`                       | `[unregistered]`         |
| Added   | `subject_territory_connectivity_with_icon`                  | `[unregistered]`         |
| Added   | `town_rights`                                               | `[unregistered]`         |
| Added   | `town_rights_icon`                                          | `[unregistered]`         |
| Added   | `town_rights_with_icon`                                     | `[unregistered]`         |
| Added   | `trade_income_share`                                        | `[unregistered]`         |
| Added   | `trade_income_share_icon`                                   | `[unregistered]`         |
| Added   | `trade_income_share_with_icon`                              | `[unregistered]`         |
| Added   | `trade_order`                                               | `[unregistered]`         |
| Added   | `trade_order_icon`                                          | `[unregistered]`         |
| Added   | `trade_order_with_icon`                                     | `[unregistered]`         |
| Added   | `trade_orders`                                              | `[unregistered]`         |
| Added   | `trade_orders_icon`                                         | `[unregistered]`         |
| Added   | `trade_orders_with_icon`                                    | `[unregistered]`         |
| Added   | `trust_equilibrium`                                         | `[unregistered]`         |
| Added   | `trust_equilibrium_icon`                                    | `[unregistered]`         |
| Added   | `trust_equilibrium_with_icon`                               | `[unregistered]`         |
| Added   | `unconditional_surrender`                                   | `[unregistered]`         |
| Added   | `unconditionally_surrender`                                 | `[unregistered]`         |
| Added   | `unconditionally_surrendered`                               | `[unregistered]`         |
| Removed | `GetCharacterInteractionIcon( Arg0 )`                       | `[unregistered]`         |
| Removed | `rite_power`                                                | `[unregistered]`         |
| Removed | `rite_power_i`                                              | `[unregistered]`         |
| Removed | `rite_power_i_icon`                                         | `[unregistered]`         |
| Removed | `rite_power_i_with_icon`                                    | `[unregistered]`         |
| Removed | `rite_power_icon`                                           | `[unregistered]`         |
| Removed | `rite_power_with_icon`                                      | `[unregistered]`         |
| Removed | `trade_efficiency`                                          | `[unregistered]`         |
| Removed | `trade_efficiency_icon`                                     | `[unregistered]`         |
| Removed | `trade_efficiency_with_icon`                                | `[unregistered]`         |

