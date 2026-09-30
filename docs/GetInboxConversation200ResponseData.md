# GetInboxConversation200ResponseData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**account_username** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: active, archived) | [optional]
**participant_name** | Option<**String**> |  | [optional]
**participant_id** | Option<**String**> |  | [optional]
**participant_verified_type** | Option<**ParticipantVerifiedType**> | X verified badge type. Only present for X conversations. (enum: blue, government, business, none) | [optional]
**business_scoped_user_id** | Option<**String**> | WhatsApp only. Meta business-scoped user ID (BSUID), the stable identity anchor; present when Meta has sent it for this participant. | [optional]
**whatsapp_username** | Option<**String**> | WhatsApp only. The participant's WhatsApp username (e.g. `jane.shop`, no leading @). Not a stable identifier, because users can change it: useful for display, not recommended as an identity anchor. Captured from inbound messages, so older threads fill in on their next inbound. | [optional]
**last_message** | Option<**String**> |  | [optional]
**last_message_at** | Option<**String**> |  | [optional]
**updated_time** | Option<**String**> |  | [optional]
**participants** | Option<[**Vec<models::UpdateFacebookPage200ResponseSelectedPage>**](UpdateFacebookPage200ResponseSelectedPage.md)> |  | [optional]
**instagram_profile** | Option<[**models::ListInboxConversations200ResponseDataInnerInstagramProfile**](ListInboxConversations200ResponseDataInnerInstagramProfile.md)> |  | [optional]
**metadata** | Option<[**models::GetInboxConversation200ResponseDataMetadata**](GetInboxConversation200ResponseDataMetadata.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


