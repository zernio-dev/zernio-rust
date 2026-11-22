# CommentAutomationDefinition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**status** | Option<**Status**> |  (enum: active, paused) | [optional][default to Active]
**trigger** | [**models::CommentAutomationDefinitionTrigger**](CommentAutomationDefinitionTrigger.md) |  | 
**or_triggers** | Option<[**Vec<models::CommentAutomationDefinitionOrTriggersInner>**](CommentAutomationDefinitionOrTriggersInner.md)> | A DM with the same keywords also starts it (`dm.keyword`), at the decision and with no comment to act on. Comment triggers with keywords only. | [optional]
**graph** | [**models::CommentAutomationDefinitionGraph**](CommentAutomationDefinitionGraph.md) |  | 
**limits** | [**models::CommentAutomationDefinitionLimits**](CommentAutomationDefinitionLimits.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


