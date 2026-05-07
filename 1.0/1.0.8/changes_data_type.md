# Release 1.0.8 - Data Type Documentation
## Global Promotes
- Added `CanUpgradeToBuilding( Arg0, Arg1 )` global promote
- Added `CanUpgradeToBuildingInfo( Arg0, Arg1 )` global promote
- Added `CharactersCanMarry( Arg0, Arg1 )` global promote
- Added `GetRankComparisonForCountryInfo( Arg0 )` global promote
- Added `StartsWith( Arg0, Arg1 )` global promote
- Added `AdvanceNode.ShowSimplifiedVersion( Arg0 )` global promote
## Types
- Added `AlertRelationAboutToBeBroken` type
- Added `AntagonismWrapper` type
## Functions
- Added `Building.GetLevelsUnderUpgrade` function
- Added `Country.CountryIsHeir( Arg0 )` function
- Added `Country.CountryIsInLineOfSuccessionNotHeir( Arg0 )` function
- Added `Country.GetEconomicalBaseWithLabel` function
- Added `Country.GetTradeByGoodForCountryInfo( Arg0 )` function
- Added `DiseaseOutbreak.GetNumLocationsForSituationView( Arg0 )` function
- Added `Estate.GetBalance` function
- Added `HeirSelection.GetKey` function
- Added `Law.GetTooltipWithCountryContext( Arg0 )` function
- Added `Law.GetTooltipWithIOContext( Arg0 )` function
- Added `Location.GetProsperityChange` function
- Added `Location.GetProsperityChangeInfo` function
- Added `Location.HasStalledConstruction` function
- Added `ResolutionGlue.HasHighestVote` function
- Added `SelectInteractionTargetView.GetNoneAvailableTextOnlyHeader` function
- Added `SubUnit.GetCurrentBoxNameInCombat` function
- Added `SubUnit.HasValidTarget` function
- Added `WarGlue.GetName` function
- Added `War.GetWarScoreOfCountry( Arg0 )` function
## Removed
- Removed `IsSelectInteractionTargetValid`
- Removed `Location.HasDiseaseOutbreak( Arg0 )`
- Removed `SubUnit.GetTargetDetails`
- Removed `SubUnit.GetTargetInfo`
- Removed `SubUnit.HasTarget`
- Removed `WarGlue.GetWar`