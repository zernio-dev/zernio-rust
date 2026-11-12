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
**facts** | Option<**std::collections::HashMap<String, serde_json::Value>**> | The event's facts as the trigger read them, keyed by fact name. Recorded only for an automation with no steps (one that only records each event).  Null for an automation with steps, whose filter results show the facts it compared, and on checks recorded before facts were kept. Content facts are null for a team that keeps no content. | 
**filter** | [**Vec<models::AutomationFactResult>**](AutomationFactResult.md) |  | 
**actions** | [**Vec<models::AutomationRunResult>**](AutomationRunResult.md) |  | 
**error** | Option<**String**> |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


