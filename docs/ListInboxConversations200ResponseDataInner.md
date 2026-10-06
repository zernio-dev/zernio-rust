# ListInboxConversations200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Opaque conversation identifier. Pass it back verbatim to any /v1/inbox/conversations/{conversationId} route; do not assume a fixed format. | [optional]
**platform** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**account_username** | Option<**String**> |  | [optional]
**participant_id** | Option<**String**> |  | [optional]
**participant_name** | Option<**String**> |  | [optional]
**participant_picture** | Option<**String**> |  | [optional]
**participant_verified_type** | Option<**ParticipantVerifiedType**> | X verified badge type. Only present for X conversations. (enum: blue, government, business, none) | [optional]
**business_scoped_user_id** | Option<**String**> | WhatsApp only. Meta business-scoped user ID (BSUID), the stable identity anchor; present when Meta has sent it for this participant. | [optional]
**whatsapp_username** | Option<**String**> | WhatsApp only. The participant's WhatsApp username (e.g. `jane.shop`, no leading @). Not a stable identifier, because users can change it: useful for display, not recommended as an identity anchor. Captured from inbound messages, so older threads fill in on their next inbound. | [optional]
**last_message** | Option<**String**> |  | [optional]
**updated_time** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: active, archived) | [optional]
**unread_count** | Option<**i32**> | Number of unread messages | [optional]
**thread_control** | Option<**ThreadControl**> | Present once a handover has touched the thread (WhatsApp, Facebook, Instagram). ai_agent: Meta Business Agent answers (WhatsApp) and new inbound arrive flagged metadata.standby; app: you hold control; other: another app does (a WhatsApp partner, or a Messenger / Instagram receiver such as Page Inbox). Change it with POST /v1/inbox/conversations/{conversationId}/thread-control. (enum: app, ai_agent, other) | [optional]
**folder** | Option<**Folder**> | Present only on items listed with folder=requests: a Message Request the account has not accepted yet. (enum: requests) | [optional]
**is_group** | Option<**bool**> | iMessage only, true for a group thread. Manage it through the /v1/imessage/groups/{conversationId} endpoints. | [optional]
**url** | Option<**String**> | Direct link to open the conversation on the platform (if available) | [optional]
**instagram_profile** | Option<[**models::ListInboxConversations200ResponseDataInnerInstagramProfile**](ListInboxConversations200ResponseDataInnerInstagramProfile.md)> |  | [optional]
**metadata** | Option<[**models::ListInboxConversations200ResponseDataInnerMetadata**](ListInboxConversations200ResponseDataInnerMetadata.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


