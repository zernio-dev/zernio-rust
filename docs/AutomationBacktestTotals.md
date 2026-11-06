# AutomationBacktestTotals

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**actions** | **i32** | Actions it would have taken. Skipped ones are not counted. | 
**pauses** | **i32** |  | 
**activations** | **i32** |  | 
**budget_raised** | **i32** | Budget changes that raised a budget. | 
**budget_lowered** | **i32** | Budget changes that lowered a budget. | 
**budget_change** | **f64** | The net budget change across every budget action, in `currency`. | 
**notifications** | **i32** |  | 
**skipped** | **i32** | Actions planned but skipped. | 
**subjects** | **i32** | Distinct objects it would have acted on. | 
**held_back** | **i32** | Matches left alone by the cooldown or a cap, summed over the days. | 
**days_with_actions** | **i32** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


