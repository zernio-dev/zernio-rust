# WebhookPayloadAutomationAlertAlert

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**subject_id** | **String** | The platform's id of the object: an ad, ad set or campaign for ad rules. | 
**severity** | Option<**Severity**> |  (enum: warning, critical, ) | 
**reason** | Option<**Reason**> | Why it resolved, on `automation.alert.resolved` only. (enum: condition_cleared, action_applied, not_evaluated, automation_changed, automation_off, ) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


