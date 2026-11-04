# WebhookPayloadAutomationCheckCompletedCheck

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**slot** | **String** | The scheduled time the check ran for. | 
**outcome** | **Outcome** |  (enum: triggered, no_match, cooldown, daily_limit, failed) | 
**subjects_evaluated** | **i32** | How many objects the check read. | 
**actions_count** | **i32** | How many actions it recorded. | 
**error** | Option<**String**> |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


