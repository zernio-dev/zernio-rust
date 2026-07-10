# OnWhatsAppAutomaticEventRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**event** | Option<**Event**> |  (enum: whatsapp.automatic_event) | [optional]
**timestamp** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> | SocialAccount id of the WhatsApp number whose conversation was flagged. | [optional]
**conversation_id** | Option<**String**> | Zernio conversation id, when the thread could be resolved. | [optional]
**platform_message_id** | Option<**String**> | The wamid of the message Meta's analysis flagged. | [optional]
**event_name** | Option<**String**> | Meta-detected event: `LeadSubmitted` | `Purchase`. | [optional]
**ctwa_clid** | Option<**String**> | Meta's CTWA click id, the Conversions API match key. | [optional]
**custom_data** | Option<[**models::OnWhatsAppAutomaticEventRequestCustomData**](OnWhatsAppAutomaticEventRequestCustomData.md)> |  | [optional]
**detected_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


