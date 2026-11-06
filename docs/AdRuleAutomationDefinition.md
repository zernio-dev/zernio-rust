# AdRuleAutomationDefinition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**status** | Option<**Status**> | A new ad rule stays paused unless `active`. (enum: active, paused) | [optional][default to Paused]
**trigger** | [**models::AutomationScheduleTrigger**](AutomationScheduleTrigger.md) |  | 
**subjects** | [**models::AutomationSubjects**](AutomationSubjects.md) |  | 
**conditions** | [**models::AdRuleConditions**](AdRuleConditions.md) |  | 
**alert** | Option<[**models::AutomationAlert**](AutomationAlert.md)> |  | [optional]
**steps** | [**Vec<models::AutomationStep>**](AutomationStep.md) |  | 
**limits** | Option<[**models::AutomationLimits**](AutomationLimits.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


