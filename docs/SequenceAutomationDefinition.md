# SequenceAutomationDefinition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**status** | Option<**Status**> | A new sequence is on unless `draft`. A draft can be activated; a sequence that ran can only be paused and activated again. (enum: draft, active, paused) | [optional][default to Active]
**trigger** | [**models::SequenceAutomationDefinitionTrigger**](SequenceAutomationDefinitionTrigger.md) |  | 
**steps** | [**Vec<models::AutomationSequenceStep>**](AutomationSequenceStep.md) | At least one step for an active sequence. Steps change only while it is a draft or paused. | 
**limits** | Option<[**models::SequenceAutomationDefinitionLimits**](SequenceAutomationDefinitionLimits.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


