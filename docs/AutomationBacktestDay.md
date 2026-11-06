# AutomationBacktestDay

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**date** | [**String**](String.md) |  | 
**checks** | **i32** | Checks the schedule would have run that day. 0 on a day it skips. | 
**evaluated** | **i32** | The most objects any of the day's checks judged. | 
**matched** | **i32** | The most objects any of the day's checks matched. | 
**held_back** | **i32** | Matches left alone all day by the cooldown or a cap. | 
**actions** | [**Vec<models::AutomationBacktestDayActionsInner>**](AutomationBacktestDayActionsInner.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


