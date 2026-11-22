# FlowAutomationDefinition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**status** | Option<**Status**> | A new flow is `draft` (the default) or `active`, which needs a complete graph. An active or paused flow never goes back to draft, and only an active flow can be paused. (enum: draft, active, paused) | [optional]
**trigger** | [**models::FlowAutomationDefinitionTrigger**](FlowAutomationDefinitionTrigger.md) |  | 
**graph** | [**models::FlowAutomationDefinitionGraph**](FlowAutomationDefinitionGraph.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


