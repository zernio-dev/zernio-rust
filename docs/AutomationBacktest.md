# AutomationBacktest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**from** | [**String**](String.md) | The first day replayed, in the ad account timezone. | 
**to** | [**String**](String.md) | The last day replayed, yesterday in the ad account timezone. | 
**timezone** | **String** |  | 
**timezone_assumed** | **bool** | True when the ad account timezone is unknown and UTC was used. | 
**currency** | Option<**String**> |  | 
**totals** | [**models::AutomationBacktestTotals**](AutomationBacktestTotals.md) |  | 
**days** | [**Vec<models::AutomationBacktestDay>**](AutomationBacktestDay.md) |  | 
**notes** | [**Vec<models::AutomationBacktestNotesInner>**](AutomationBacktestNotesInner.md) | What this replay could not know, for example that budgets have no history. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


