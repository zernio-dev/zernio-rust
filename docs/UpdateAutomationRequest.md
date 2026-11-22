# UpdateAutomationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**description** | Option<**String**> | Sequences and flows. | [optional]
**status** | Option<**Status**> | `draft` only for a sequence or a flow that has not left draft. (enum: draft, active, paused) | [optional]
**trigger** | Option<**serde_json::Value**> | The trigger of the automation's kind. | [optional]
**or_triggers** | Option<**Vec<serde_json::Value>**> | Comment to DM. | [optional]
**graph** | Option<**serde_json::Value**> | Comment to DM and flows: the whole graph, as read. | [optional]
**subjects** | Option<[**models::UpdateAutomationRequestSubjects**](UpdateAutomationRequestSubjects.md)> |  | [optional]
**filter** | Option<[**models::AutomationFactCondition**](AutomationFactCondition.md)> |  | [optional]
**conditions** | Option<[**models::AdRuleConditions**](AdRuleConditions.md)> |  | [optional]
**alert** | Option<[**models::AutomationAlert**](AutomationAlert.md)> |  | [optional]
**steps** | Option<[**Vec<models::UpdateAutomationRequestStepsInner>**](UpdateAutomationRequestStepsInner.md)> | The steps the automation's kind takes. | [optional]
**limits** | Option<**serde_json::Value**> | The limits of the automation's kind. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


