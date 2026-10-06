# WebhookPayloadConversationControlChangedControl

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**owner** | **Owner** | Who answers now. ai_agent: Meta Business Agent (WhatsApp); app: you; other: another app (a WhatsApp partner, or a Messenger / Instagram receiver such as Page Inbox). (enum: app, ai_agent, other) | 
**previous_owner** | Option<**PreviousOwner**> | Owner before this change, null when no handover had touched the thread. (enum: app, ai_agent, other, ) | 
**owner_app_id** | Option<**String**> | Meta app id of the new owner, when Meta names it (Facebook and Instagram handovers, WhatsApp partner apps). Page Inbox is 263902037430900. | [optional]
**metadata** | Option<**String**> | Free-form string the transferring app attached to the handover, forwarded verbatim. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


