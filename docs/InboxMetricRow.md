# InboxMetricRow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**date** | **String** | Start of the period: the day or the Monday of the week, never before fromDate. With granularity=total, fromDate. | 
**account_id** | Option<**String**> | With groupBy=account. | [optional]
**platform** | Option<**String**> | With groupBy=account or groupBy=platform. | [optional]
**source** | Option<**String**> | With groupBy=source; null for messages with no source recorded, such as messages received. | [optional]
**day_of_week** | Option<**i32**> | With groupBy=hourOfWeek: 1 is Monday, 7 is Sunday, in UTC. | [optional]
**hour** | Option<**i32**> | With groupBy=hourOfWeek: 0 to 23, in UTC. | [optional]
**response_time_bucket** | Option<[**models::ResponseTimeBucket**](ResponseTimeBucket.md)> | With groupBy=responseTimeBucket. | [optional]
**account** | Option<[**models::InboxMetricRowAccount**](InboxMetricRowAccount.md)> |  | [optional]
**conversation_id** | Option<**String**> | With groupBy=conversation or conversationId: the Zernio conversation id, or the id logged with the messages when the conversation no longer exists. | [optional]
**first_message_at** | Option<**String**> | With conversation rows: first message, read receipt or failure in the period, UTC. null for a conversation read by id with no activity in the period. | [optional]
**last_message_at** | Option<**String**> | With conversation rows: last message, read receipt or failure in the period, UTC. | [optional]
**conversation** | Option<[**models::InboxMetricRowConversation**](InboxMetricRowConversation.md)> |  | [optional]
**metrics** | **std::collections::HashMap<String, f64>** | Each metric asked; response times are null when no message received got a reply. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


