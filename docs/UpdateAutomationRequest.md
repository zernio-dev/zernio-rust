# UpdateAutomationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: active, paused) | [optional]
**trigger** | Option<[**models::AutomationTrigger**](AutomationTrigger.md)> |  | [optional]
**subjects** | Option<[**models::UpdateAutomationRequestSubjects**](UpdateAutomationRequestSubjects.md)> |  | [optional]
**filter** | Option<[**models::AutomationFactCondition**](AutomationFactCondition.md)> |  | [optional]
**conditions** | Option<[**models::AdRuleConditions**](AdRuleConditions.md)> |  | [optional]
**alert** | Option<[**models::AutomationAlert**](AutomationAlert.md)> |  | [optional]
**steps** | Option<[**Vec<models::UpdateAutomationRequestStepsInner>**](UpdateAutomationRequestStepsInner.md)> | The steps the automation's kind takes. | [optional]
**limits** | Option<[**models::UpdateAutomationRequestLimits**](UpdateAutomationRequestLimits.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


