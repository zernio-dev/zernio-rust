# EventAutomationCheck

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**automation_id** | **String** |  | 
**checked_at** | **String** |  | 
**outcome** | **Outcome** |  (enum: triggered, no_match, cooldown, daily_limit, failed) | 
**evaluated** | **i32** |  | 
**event** | Option<**String**> |  | 
**event_id** | Option<**String**> |  | 
**subject** | [**models::EventAutomationCheckSubject**](EventAutomationCheckSubject.md) |  | 
**filter** | [**Vec<models::AutomationFactResult>**](AutomationFactResult.md) |  | 
**actions** | [**Vec<models::AutomationRunResult>**](AutomationRunResult.md) |  | 
**error** | Option<**String**> |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


