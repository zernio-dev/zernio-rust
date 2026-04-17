# WebhookPayloadMessageMetadata

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**quick_reply_payload** | Option<**String**> | Payload from a quick reply tap (Facebook/Instagram Messenger). | [optional]
**postback_payload** | Option<**String**> | Payload from a postback button tap (Facebook/Instagram Messenger). | [optional]
**postback_title** | Option<**String**> | Title of the tapped postback button (Facebook/Instagram Messenger). | [optional]
**callback_data** | Option<**String**> | Callback data from an inline keyboard button tap (Telegram). | [optional]
**interactive_type** | Option<**InteractiveType**> | WhatsApp only. Which kind of interactive reply the user sent: `button_reply` (tap on an interactive button), `list_reply` (tap on a list row), or `nfm_reply` (a WhatsApp Flow submission).  (enum: button_reply, list_reply, nfm_reply) | [optional]
**interactive_id** | Option<**String**> | WhatsApp only. The `id` of the tapped button or list row, matching the `id` you supplied when the message was sent. Not set for Flow responses.  | [optional]
**button_payload** | Option<**String**> | WhatsApp only. Payload attached to a tapped template button. Template buttons emit a plain `button` webhook (not an interactive reply), so `interactiveType` is empty while this field is populated.  | [optional]
**flow_response_json** | Option<**String**> | WhatsApp only. Raw `nfm_reply.response_json` string returned by a Flow submission. Useful if you need the exact wire payload; for typed access use `flowResponseData` instead.  | [optional]
**flow_response_data** | Option<**std::collections::HashMap<String, serde_json::Value>**> | WhatsApp only. Parsed Flow response JSON. Populated when `flowResponseJson` is valid JSON; otherwise omitted. Keys and value types depend on the specific Flow that was submitted.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


