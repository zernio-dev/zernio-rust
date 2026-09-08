# WebhookPayloadConversationControlChangedControl

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**owner** | **Owner** | Who answers now. ai_agent: Meta Business Agent; app: you; other: another partner app on the number. (enum: app, ai_agent, other) | 
**previous_owner** | Option<**PreviousOwner**> | Owner before this change, null when the thread had never been agent-handled. (enum: app, ai_agent, other, ) | 
**metadata** | Option<**String**> | Free-form string the transferring app attached to the handover, forwarded verbatim. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


