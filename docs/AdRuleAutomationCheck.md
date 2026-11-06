# AdRuleAutomationCheck

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**automation_id** | **String** |  | 
**checked_at** | **String** |  | 
**outcome** | **Outcome** |  (enum: triggered, cooldown, no_match, failed) | 
**evaluated** | **i32** | Objects judged. | 
**subjects** | [**Vec<models::AdRuleAutomationCheckSubjectsInner>**](AdRuleAutomationCheckSubjectsInner.md) |  | 
**actions** | [**Vec<models::AdRuleAutomationCheckActionsInner>**](AdRuleAutomationCheckActionsInner.md) |  | 
**notification** | [**models::AdRuleAutomationCheckNotification**](AdRuleAutomationCheckNotification.md) |  | 
**error** | Option<**String**> |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


