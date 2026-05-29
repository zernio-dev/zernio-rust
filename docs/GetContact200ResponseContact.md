# GetContact200ResponseContact

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**email** | Option<**String**> |  | [optional]
**company** | Option<**String**> |  | [optional]
**avatar_url** | Option<**String**> |  | [optional]
**tags** | Option<**Vec<String>**> |  | [optional]
**is_subscribed** | Option<**bool**> |  | [optional]
**is_blocked** | Option<**bool**> |  | [optional]
**messages_sent_count** | Option<**i32**> | Messages sent to the contact, derived live from message history across all linked conversations. | [optional]
**messages_received_count** | Option<**i32**> | Messages received from the contact, derived live from message history across all linked conversations. | [optional]
**last_message_sent_at** | Option<**String**> | Timestamp of the most recent outgoing message, or null if none. | [optional]
**last_message_received_at** | Option<**String**> | Timestamp of the most recent incoming message, or null if none. | [optional]
**custom_fields** | Option<**serde_json::Value**> |  | [optional]
**notes** | Option<**String**> |  | [optional]
**conversation_ids** | Option<**Vec<String>**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


