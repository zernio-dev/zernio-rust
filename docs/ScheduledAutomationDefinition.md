# ScheduledAutomationDefinition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**status** | Option<**Status**> | A new scheduled automation is on unless `paused`. (enum: active, paused) | [optional][default to Active]
**trigger** | [**models::AutomationPostSchedule**](AutomationPostSchedule.md) |  | 
**subjects** | [**models::AutomationPostSubjects**](AutomationPostSubjects.md) |  | 
**filter** | Option<[**models::AutomationFactCondition**](AutomationFactCondition.md)> |  | [optional]
**steps** | [**Vec<models::ScheduledAutomationDefinitionStepsInner>**](ScheduledAutomationDefinitionStepsInner.md) |  | 
**limits** | Option<[**models::AutomationEventLimits**](AutomationEventLimits.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


