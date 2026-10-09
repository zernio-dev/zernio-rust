# WebhookPayloadWhatsAppContactIdentityChanged

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. It identifies the event only, never an account or other resource. | 
**test** | Option<**bool**> | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional]
**event** | **Event** |  (enum: whatsapp.contact.identity_changed) | 
**account** | [**models::WebhookPayloadWhatsAppAccountQualityUpdatedAccount**](WebhookPayloadWhatsAppAccountQualityUpdatedAccount.md) |  | 
**reason** | **Reason** | Which Meta signal reported the change. `user_changed_number`: new phone number. `user_changed_user_id` and `user_id_update`: new BSUID. (enum: user_changed_number, user_changed_user_id, user_identity_changed, user_id_update) | 
**previous** | [**models::WhatsAppContactIdentity**](WhatsAppContactIdentity.md) |  | 
**current** | [**models::WhatsAppContactIdentity**](WhatsAppContactIdentity.md) |  | 
**contact_id** | Option<**String**> | Zernio contact id matched on the new identity, null when none exists yet. | 
**conversation_id** | Option<**String**> | Zernio inbox conversation that was re-keyed, null when there was none. | 
**changed_at** | **String** | When Meta reported the change. | 
**timestamp** | **String** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


