# ScheduledAutomationCheck

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**automation_id** | **String** |  | 
**checked_at** | **String** |  | 
**outcome** | **Outcome** |  (enum: triggered, no_match, cooldown, daily_limit, failed) | 
**evaluated** | **i32** | Posts judged. | 
**analytics_synced_at** | Option<**String**> | The oldest analytics sync among the posts judged: their numbers are as of then. | 
**matched** | [**Vec<models::ScheduledAutomationCheckMatchedInner>**](ScheduledAutomationCheckMatchedInner.md) | Up to 20 matching posts. | 
**actions** | [**Vec<models::ScheduledAutomationCheckActionsInner>**](ScheduledAutomationCheckActionsInner.md) |  | 
**error** | Option<**String**> |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


