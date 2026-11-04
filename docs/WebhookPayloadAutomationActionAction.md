# WebhookPayloadAutomationActionAction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**subject_id** | **String** | The platform's id of the object changed: an ad, ad set or campaign for ad rules. | 
**r#type** | **String** | `pause`, `activate`, `adjust_budget` or `notify` for ad rules. New values may be added. | 
**status** | **Status** |  (enum: applied, skipped, failed, unknown) | 
**reason** | Option<**String**> |  | 
**previous** | Option<**std::collections::HashMap<String, serde_json::Value>**> | The value before the change, such as `{ \"dailyBudget\": 40 }`. | 
**target** | Option<**std::collections::HashMap<String, serde_json::Value>**> | The value the change sets, such as `{ \"dailyBudget\": 48 }` or `{ \"status\": \"paused\" }`. | 
**acted_at** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


