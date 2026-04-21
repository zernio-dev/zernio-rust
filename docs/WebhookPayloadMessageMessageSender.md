# WebhookPayloadMessageMessageSender

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Sender's platform identifier. For WhatsApp this is the phone number (without leading `+`) when available, otherwise the `businessScopedUserId`.  | 
**name** | Option<**String**> |  | [optional]
**username** | Option<**String**> |  | [optional]
**picture** | Option<**String**> |  | [optional]
**phone_number** | Option<**String**> | WhatsApp only. Sender's phone number in E.164 format (with leading `+`).  **Nullable during the BSUID rollout (April 2026+).** WhatsApp users who adopt a username can message businesses without exposing a phone number — this field is omitted for them. Match by `businessScopedUserId` instead. See `docs/whatsapp-bsuid-migration.md`.  | [optional]
**business_scoped_user_id** | Option<**String**> | WhatsApp only. Business-scoped user ID (BSUID) — Meta's canonical identifier for a WhatsApp user within your business. Present when Meta includes it in the inbound payload (rollout in progress since early April 2026). **Recommended primary identity anchor** going forward; fall back to `phoneNumber` only when this field is absent.  | [optional]
**parent_business_scoped_user_id** | Option<**String**> | WhatsApp only. Parent BSUID for businesses with linked business portfolios. Omitted for standalone portfolios.  | [optional]
**whatsapp_username** | Option<**String**> | WhatsApp only. User's WhatsApp username (e.g. `@jane`). Not a stable identifier — users can change it. Useful for display, not recommended as an identity anchor.  | [optional]
**instagram_profile** | Option<[**models::WebhookPayloadMessageMessageSenderInstagramProfile**](WebhookPayloadMessageMessageSenderInstagramProfile.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


