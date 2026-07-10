# Data Type Documentation 1.3
## Table of Contents
 * [Types](#types)
 * [Global Functions](#global-functions)
 * [Global Promotes](#global-promotes)
## Notes
This is just a very basic overview of added and removed data types.

Changed elements are **not** mentioned here.
## Types
| Type | Data Type |
|--|--|
| Added | `ChivalricOrder` |
| Added | `ImperialCircle` |
| Added | `AlertCanArrangeInternationalMarriage` |
| Added | `AlertExpiringContracts` |
| Added | `AlertHasImminentIndependenceWar` |
| Added | `AlertMercenariesInTrouble` |
| Added | `AutoTableWidth` |
| Added | `ChivalricOrder` |
| Added | `CircleActionItem` |
| Added | `CountryCultureLateralViewArtistItem` |
| Added | `CreditLateralView` |
| Added | `DispositionPairWrap` |
| Added | `EstateActionsLateralView` |
| Added | `GagCountryItem` |
| Added | `GagFactionItem` |
| Added | `GovernmentReformAgeGroup` |
| Added | `GovernmentReformsPerAgeLateralView` |
| Added | `IconAndText` |
| Added | `ImperialCircle` |
| Added | `ImperialCircleItem` |
| Added | `IndependenceMovementIOView` |
| Added | `IssueElement` |
| Added | `ItalianWarsCountryItem` |
| Added | `ItalianWarsLeagueItem` |
| Added | `ItalianWarsLeaguePieSlice` |
| Added | `ItalianWarsWarItem` |
| Added | `ParliamentRowItem` |
| Added | `PaymentPayerPriceWrap` |
| Added | `QuickBuildingTypeInfo` |
| Added | `QuickChivalricOrderMembers` |
| Added | `QuickNotableDispositions` |
| Added | `QuickTradeOrders` |
| Added | `QuickTriggerDesc` |
| Added | `RebelMovementGlue` |
| Added | `ReformationCountryItem` |
| Added | `ReformationMovementCountryItem` |
| Added | `ReformationMovementItem` |
| Added | `ReformationPieSliceItem` |
| Added | `ReformationPopReligionSlice` |
| Added | `ReformationPopTypePie` |
| Added | `ReformationReligionItem` |
| Added | `SpyNetworkFogWrap` |
| Added | `UnitAdjustedCount` |
| Added | `WinterBlockedMarker` |
| Removed | `MercenaryModifierWrap` |  |
| Removed | `PlayerPlayStyleItem` |  |
| Removed | `SelectLoanLateralView` |  |

## Global Functions
| Type | Function | Return Type |
|--|--|--|
| Added | `AreBuildingsAutoExpand( Arg0 )` | `bool` |
| Added | `BoolToFrame( Arg0 )` | `int32` |
| Added | `ChangeReformInGovernmentReformsPerAgeLateralView( Arg0 )` | `void` |
| Added | `DynTr( Arg0 )` | `CString` |
| Added | `GameWouldBeIronman` | `bool` |
| Added | `GetChivalricOrderIcon( Arg0 )` | `[unregistered]` |
| Added | `GetPauseBannerLabel` | `CString` |
| Added | `GetRepayAllLoansConditionsForPlayer` | `CString` |
| Added | `GetRepayAllLoansCostForPlayer` | `CString` |
| Added | `GetRepayAllLoansDescriptionForPlayer` | `CString` |
| Added | `GetRepayAllPossibleLoansCostForPlayer` | `CString` |
| Added | `GetSubunitTypeIllustrationMaskPreview( Arg0, Arg1 )` | `[unregistered]` |
| Added | `GetSubunitTypeIllustrationPreview( Arg0, Arg1 )` | `[unregistered]` |
| Added | `HasAiPersonalityIntelOn( Arg0 )` | `bool` |
| Added | `HasArmySizeIntelOn( Arg0 )` | `bool` |
| Added | `HasArmyTraditionIntelOn( Arg0 )` | `bool` |
| Added | `HasAttritionIntelOn( Arg0 )` | `bool` |
| Added | `HasAvailableSlotsIntelOn( Arg0 )` | `bool` |
| Added | `HasCombatModifiersIntelOn( Arg0 )` | `bool` |
| Added | `HasConstructionsIntelOn( Arg0 )` | `bool` |
| Added | `HasCountryModifiersIntelOn( Arg0 )` | `bool` |
| Added | `HasDevelopmentIntelOn( Arg0 )` | `bool` |
| Added | `HasDiseaseIntelOn( Arg0 )` | `bool` |
| Added | `HasEmploymentIntelOn( Arg0 )` | `bool` |
| Added | `HasEnfranchisementIntelOn( Arg0 )` | `bool` |
| Added | `HasEstatesPowerIntelOn( Arg0 )` | `bool` |
| Added | `HasFoodDecayIntelOn( Arg0 )` | `bool` |
| Added | `HasFoodOutputIntelOn( Arg0 )` | `bool` |
| Added | `HasFortCountIntelOn( Arg0 )` | `bool` |
| Added | `HasFortLevelIntelOn( Arg0 )` | `bool` |
| Added | `HasGarrisonIntelOn( Arg0 )` | `bool` |
| Added | `HasIncomeIntelOn( Arg0 )` | `bool` |
| Added | `HasIntegrationIntelOn( Arg0 )` | `bool` |
| Added | `HasLegitimacyIntelOn( Arg0 )` | `bool` |
| Added | `HasLevyStrengthIntelOn( Arg0 )` | `bool` |
| Added | `HasLiteracyIntelOn( Arg0 )` | `bool` |
| Added | `HasLocationLeviesIntelOn( Arg0 )` | `bool` |
| Added | `HasLocationModifiersIntelOn( Arg0 )` | `bool` |
| Added | `HasLocationTaxBaseIntelOn( Arg0 )` | `bool` |
| Added | `HasManpowerIntelOn( Arg0 )` | `bool` |
| Added | `HasMigrationIntelOn( Arg0 )` | `bool` |
| Added | `HasMovementResistanceIntelOn( Arg0 )` | `bool` |
| Added | `HasNavyLevyStrengthIntelOn( Arg0 )` | `bool` |
| Added | `HasNavyStrengthIntelOn( Arg0 )` | `bool` |
| Added | `HasNavyTraditionIntelOn( Arg0 )` | `bool` |
| Added | `HasOwnershipIntelOn( Arg0 )` | `bool` |
| Added | `HasPopBreakdownIntelOn( Arg0 )` | `bool` |
| Added | `HasProsperityIntelOn( Arg0 )` | `bool` |
| Added | `HasRawMaterialsIntelOn( Arg0 )` | `bool` |
| Added | `HasRgoWorkersIntelOn( Arg0 )` | `bool` |
| Added | `HasRulerStatsIntelOn( Arg0 )` | `bool` |
| Added | `HasSailorsIntelOn( Arg0 )` | `bool` |
| Added | `HasSatisfactionIntelOn( Arg0 )` | `bool` |
| Added | `HasStabilityIntelOn( Arg0 )` | `bool` |
| Added | `HasSupplyLimitIntelOn( Arg0 )` | `bool` |
| Added | `HasTaxBaseIntelOn( Arg0 )` | `bool` |
| Added | `HasTotalPopulationIntelOn( Arg0 )` | `bool` |
| Added | `HasTradeVolumesIntelOn( Arg0 )` | `bool` |
| Added | `HasWarExhaustionIntelOn( Arg0 )` | `bool` |
| Added | `HasWarWorthIntelOn( Arg0 )` | `bool` |
| Added | `IsAutoExpand( Arg0 )` | `bool` |
| Added | `IsAutoExpandRGO( Arg0 )` | `bool` |
| Added | `IsDispositionMapPerspectivePlayer` | `bool` |
| Added | `IsPlayerAlliedWithOtherPlayerInWar( Arg0 )` | `bool` |
| Added | `IsRepayAllLoansEnabledForPlayer` | `bool` |
| Added | `IsRepayAllPossibleLoansEnabledForPlayer` | `bool` |
| Added | `ListNotAutomatedMarkets` | `CString` |
| Added | `MoveCapitalHere( Arg0 )` | `void` |
| Added | `OnChangedFreeAutomatedTradeCapacity( Arg0 )` | `void` |
| Added | `OnRepayAllLoansForPlayer` | `void` |
| Added | `OnRepayAllPossibleLoansForPlayer` | `void` |
| Added | `OpenMarketTradesTabWithImportExportFilter( Arg0, Arg1 )` | `void` |
| Added | `PlayUIEffect( Arg0 )` | `void` |
| Added | `SelectLocationToBuildByKey( Arg0 )` | `void` |
| Added | `SetIconAndTextFromTextContext( Arg0 )` | `void` |
| Added | `ShowChivalricOrderName( Arg0 )` | `CString` |
| Added | `ShowChivalricOrderNameWithNoTooltip( Arg0 )` | `CString` |
| Added | `ShowCountryAdvancesView` | `void` |
| Added | `ShowJominiPrivacyPolicy` | `void` |
| Added | `ShowJominiUserAgreement` | `void` |
| Added | `ShowSocietyDirectionIcon( Arg0 )` | `CString` |
| Added | `ShowSocietyDirectionNameWithIcon( Arg0 )` | `CString` |
| Added | `ToggleAutoExpandBuilding( Arg0 )` | `void` |
| Added | `ToggleAutoExpandBuildings( Arg0 )` | `void` |
| Added | `ToggleAutoExpandRGO( Arg0 )` | `void` |
| Added | `alliance_bloc` | `[unregistered]` |
| Added | `alliance_bloc_icon` | `[unregistered]` |
| Added | `alliance_bloc_with_icon` | `[unregistered]` |
| Added | `alliance_blocs` | `[unregistered]` |
| Added | `alliance_blocs_icon` | `[unregistered]` |
| Added | `alliance_blocs_with_icon` | `[unregistered]` |
| Added | `bond_interest` | `[unregistered]` |
| Added | `bond_interest_icon` | `[unregistered]` |
| Added | `bond_interest_with_icon` | `[unregistered]` |
| Added | `bureaucracy_type` | `[unregistered]` |
| Added | `bureaucracy_type_icon` | `[unregistered]` |
| Added | `bureaucracy_type_with_icon` | `[unregistered]` |
| Added | `central_bank` | `[unregistered]` |
| Added | `central_bank_icon` | `[unregistered]` |
| Added | `central_bank_with_icon` | `[unregistered]` |
| Added | `chivalric_order` | `[unregistered]` |
| Added | `chivalric_order_icon` | `[unregistered]` |
| Added | `chivalric_order_with_icon` | `[unregistered]` |
| Added | `chivalric_orders` | `[unregistered]` |
| Added | `chivalric_orders_icon` | `[unregistered]` |
| Added | `chivalric_orders_with_icon` | `[unregistered]` |
| Added | `circle_leader` | `[unregistered]` |
| Added | `circle_leader_icon` | `[unregistered]` |
| Added | `circle_leader_with_icon` | `[unregistered]` |
| Added | `circle_leaders` | `[unregistered]` |
| Added | `circle_leaders_icon` | `[unregistered]` |
| Added | `circle_leaders_with_icon` | `[unregistered]` |
| Added | `circle_satisfaction` | `[unregistered]` |
| Added | `circle_satisfaction_icon` | `[unregistered]` |
| Added | `circle_satisfaction_with_icon` | `[unregistered]` |
| Added | `conquest` | `[unregistered]` |
| Added | `conquest_icon` | `[unregistered]` |
| Added | `conquest_with_icon` | `[unregistered]` |
| Added | `court_dialect` | `[unregistered]` |
| Added | `court_dialect_icon` | `[unregistered]` |
| Added | `court_dialect_with_icon` | `[unregistered]` |
| Added | `creditworthiness` | `[unregistered]` |
| Added | `creditworthiness_icon` | `[unregistered]` |
| Added | `creditworthiness_with_icon` | `[unregistered]` |
| Added | `establishment` | `[unregistered]` |
| Added | `establishment_icon` | `[unregistered]` |
| Added | `establishment_with_icon` | `[unregistered]` |
| Added | `estate_culture` | `[unregistered]` |
| Added | `estate_culture_icon` | `[unregistered]` |
| Added | `estate_culture_with_icon` | `[unregistered]` |
| Added | `estate_cultures` | `[unregistered]` |
| Added | `estate_cultures_icon` | `[unregistered]` |
| Added | `estate_cultures_with_icon` | `[unregistered]` |
| Added | `estate_religion` | `[unregistered]` |
| Added | `estate_religion_icon` | `[unregistered]` |
| Added | `estate_religion_with_icon` | `[unregistered]` |
| Added | `estate_religions` | `[unregistered]` |
| Added | `estate_religions_icon` | `[unregistered]` |
| Added | `estate_religions_with_icon` | `[unregistered]` |
| Added | `ethnicity` | `[unregistered]` |
| Added | `ethnicity_icon` | `[unregistered]` |
| Added | `ethnicity_with_icon` | `[unregistered]` |
| Added | `gdp_per_capita` | `[unregistered]` |
| Added | `gdp_per_capita_icon` | `[unregistered]` |
| Added | `gdp_per_capita_with_icon` | `[unregistered]` |
| Added | `government_bond` | `[unregistered]` |
| Added | `government_bond_icon` | `[unregistered]` |
| Added | `government_bond_with_icon` | `[unregistered]` |
| Added | `government_bonds` | `[unregistered]` |
| Added | `government_bonds_icon` | `[unregistered]` |
| Added | `government_bonds_with_icon` | `[unregistered]` |
| Added | `graphical_culture` | `[unregistered]` |
| Added | `graphical_culture_icon` | `[unregistered]` |
| Added | `graphical_culture_with_icon` | `[unregistered]` |
| Added | `great_power_points` | `[unregistered]` |
| Added | `great_power_points_icon` | `[unregistered]` |
| Added | `great_power_points_short` | `[unregistered]` |
| Added | `great_power_points_short_icon` | `[unregistered]` |
| Added | `great_power_points_short_with_icon` | `[unregistered]` |
| Added | `great_power_points_with_icon` | `[unregistered]` |
| Added | `heathenry` | `[unregistered]` |
| Added | `heathenry_icon` | `[unregistered]` |
| Added | `heathenry_with_icon` | `[unregistered]` |
| Added | `heresy` | `[unregistered]` |
| Added | `heresy_icon` | `[unregistered]` |
| Added | `heresy_with_icon` | `[unregistered]` |
| Added | `imperial_circle` | `[unregistered]` |
| Added | `imperial_circle_icon` | `[unregistered]` |
| Added | `imperial_circle_with_icon` | `[unregistered]` |
| Added | `imperial_circles` | `[unregistered]` |
| Added | `imperial_circles_icon` | `[unregistered]` |
| Added | `imperial_circles_with_icon` | `[unregistered]` |
| Added | `liturgical_dialect` | `[unregistered]` |
| Added | `liturgical_dialect_icon` | `[unregistered]` |
| Added | `liturgical_dialect_with_icon` | `[unregistered]` |
| Added | `regional_power` | `[unregistered]` |
| Added | `regional_power_icon` | `[unregistered]` |
| Added | `regional_power_with_icon` | `[unregistered]` |
| Added | `regional_powers` | `[unregistered]` |
| Added | `regional_powers_icon` | `[unregistered]` |
| Added | `regional_powers_with_icon` | `[unregistered]` |
| Added | `secondary_culture` | `[unregistered]` |
| Added | `secondary_culture_icon` | `[unregistered]` |
| Added | `secondary_culture_with_icon` | `[unregistered]` |
| Added | `situation_tension` | `[unregistered]` |
| Added | `situation_tension_icon` | `[unregistered]` |
| Added | `situation_tension_with_icon` | `[unregistered]` |
| Added | `spy_network_fog` | `[unregistered]` |
| Added | `spy_network_fog_icon` | `[unregistered]` |
| Added | `spy_network_fog_with_icon` | `[unregistered]` |
| Added | `unconditionally_surrenders` | `[unregistered]` |
| Added | `wealth_impact` | `[unregistered]` |
| Added | `wealth_impact_icon` | `[unregistered]` |
| Added | `wealth_impact_with_icon` | `[unregistered]` |
| Removed | `CanCreateMarketInLocation( Arg0 )` | `bool` |
| Removed | `CanCreateMarketInLocationTooltip( Arg0 )` | `CString` |
| Removed | `CanDestroyMarketInLocation( Arg0 )` | `bool` |
| Removed | `CanDestroyMarketInLocationTooltip( Arg0 )` | `CString` |
| Removed | `GetCreateMarketInLocationPrice( Arg0 )` | `CString` |
| Removed | `OpenFileDirectory( Arg0 )` | `void` |
| Removed | `ShowMoveCapital( Arg0 )` | `bool` |

## Global Promotes
| Type | Promote | Return Type |
|--|--|--|
| Added | `CHIVALRIC_ORDER` | `` |
| Added | `CHIVALRIC_ORDER` | `` |
| Added | `GetAutoTableWidthFor( Arg0 )` | `` |
| Added | `GetAutoTableWidthFor( Arg0 )` | `` |
| Added | `GetQuickBuildingTypeInfo( Arg0 )` | `` |
| Added | `GetQuickBuildingTypeInfo( Arg0 )` | `` |
| Added | `GetQuickChivalricOrderMembers( Arg0 )` | `` |
| Added | `GetQuickChivalricOrderMembers( Arg0 )` | `` |
| Added | `GetQuickNotableDispositions( Arg0 )` | `` |
| Added | `GetQuickNotableDispositions( Arg0 )` | `` |
| Added | `GetQuickTradeOrders( Arg0 )` | `` |
| Added | `GetQuickTradeOrders( Arg0 )` | `` |
| Added | `GetQuickUnitAdjustedCount( Arg0 )` | `` |
| Added | `GetQuickUnitAdjustedCount( Arg0 )` | `` |
| Added | `IMPERIAL_CIRCLE` | `` |
| Added | `IMPERIAL_CIRCLE` | `` |
| Added | `ImportExportModeGetView` | `` |
| Added | `ImportExportModeGetView` | `` |
| Added | `StringToIconAndText( Arg0 )` | `` |
| Added | `StringToIconAndText( Arg0 )` | `` |
| Added | `TARGET_CHIVALRIC_ORDER` | `` |
| Added | `TARGET_CHIVALRIC_ORDER` | `` |
| Added | `TARGET_IMPERIAL_CIRCLE` | `` |
| Added | `TARGET_IMPERIAL_CIRCLE` | `` |

