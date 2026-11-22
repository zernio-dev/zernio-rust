# AutomationOneOf4

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**status** | **Status** | Only a sequence can be a draft. (enum: draft, active, paused) | 
**trigger** | [**models::CommentAutomationDefinitionTrigger**](CommentAutomationDefinitionTrigger.md) |  | 
**or_triggers** | Option<[**Vec<models::CommentAutomationDefinitionOrTriggersInner>**](CommentAutomationDefinitionOrTriggersInner.md)> | A DM with the same keywords also starts it (`dm.keyword`), at the decision and with no comment to act on. Comment triggers with keywords only. | [optional]
**graph** | [**models::CommentAutomationDefinitionGraph**](CommentAutomationDefinitionGraph.md) |  | 
**limits** | [**models::CommentAutomationDefinitionLimits**](CommentAutomationDefinitionLimits.md) |  | 
**id** | **String** |  | 
**kind** | **Kind** |  (enum: comment) | 
**version** | **String** | Send it back as `If-Match` when editing, so an edit made after someone else saved is refused. | 
**last_check_at** | **String** | Null until an ad rule first checks. Always null for event and scheduled automations; their checks list when they ran. | 
**next_check_at** | **String** | Null while paused. Always null for event, scheduled and sequence automations. | 
**created_at** | **String** |  | 
**updated_at** | **String** |  | 
**template** | Option<[**models::AutomationRecordTemplate**](AutomationRecordTemplate.md)> |  | [optional]
**platform** | **String** | The account's platform. On TikTok, Threads, LinkedIn and YouTube it only posts the public reply. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


