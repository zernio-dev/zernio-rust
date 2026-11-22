# AutomationOneOf4

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**status** | **Status** | Only a sequence or a flow can be a draft. (enum: draft, active, paused) | 
**trigger** | [**models::CommentAutomationDefinitionTrigger**](CommentAutomationDefinitionTrigger.md) |  | 
**or_triggers** | Option<[**Vec<models::CommentAutomationDefinitionOrTriggersInner>**](CommentAutomationDefinitionOrTriggersInner.md)> | A DM with the same keywords also starts it (`dm.keyword`), at the decision and with no comment to act on. Comment triggers with keywords only. | [optional]
**graph** | [**models::CommentAutomationDefinitionGraph**](CommentAutomationDefinitionGraph.md) |  | 
**limits** | [**models::CommentAutomationDefinitionLimits**](CommentAutomationDefinitionLimits.md) |  | 
**id** | **String** |  | 
**kind** | **Kind** |  (enum: comment) | 
**version** | **String** | Send it back as `If-Match` when editing, so an edit made after someone else saved is refused. | 
**last_check_at** | **String** | Null until an ad rule first checks. Always null for every other kind; the checks of event and scheduled automations list when they ran. | 
**next_check_at** | **String** | Null while paused. Always null for every kind but ad rules. | 
**created_at** | **String** |  | 
**updated_at** | **String** |  | 
**template** | Option<[**models::AutomationRecordTemplate**](AutomationRecordTemplate.md)> |  | [optional]
**platform** | **String** | The account's platform. On TikTok, Threads, LinkedIn and YouTube it only posts the public reply. | 
**read_only** | Option<**bool**> | Always true when present. Present when the graph only comes near what the automation does. It is read here and edited through `/v1/comment-automations`; an edit here is refused. | [optional]
**stats** | [**models::AutomationOneOf4AllOfStats**](AutomationOneOf4AllOfStats.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


