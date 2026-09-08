# BusinessAgentSkill

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | Option<**String**> | Lowercase letters, digits and hyphens, e.g. greeting-skill. | [optional]
**description** | Option<**String**> | When the agent should apply the skill. | [optional]
**skill** | **String** | The instructions themselves. Avoid two skills that both claim priority for the same situation. | 
**id** | **String** |  | 
**channel** | Option<**String**> |  | [optional]
**created_at** | Option<**i32**> | Unix seconds. | [optional]
**status** | Option<**Status**> | pending_review right after a write; blocked means Meta content review rejected it and the agent never applies it. (enum: active, pending_review, blocked) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


