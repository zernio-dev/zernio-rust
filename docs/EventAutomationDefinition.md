# EventAutomationDefinition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**status** | Option<**Status**> | A new event automation is on unless `paused`. (enum: active, paused) | [optional][default to Active]
**trigger** | [**models::AutomationEventTrigger**](AutomationEventTrigger.md) |  | 
**steps** | [**Vec<models::AutomationNotifyStep>**](AutomationNotifyStep.md) |  | 
**limits** | Option<[**models::AutomationEventLimits**](AutomationEventLimits.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


