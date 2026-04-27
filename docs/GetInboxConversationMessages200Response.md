# GetInboxConversationMessages200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | Option<**String**> |  | [optional]
**pagination** | Option<[**models::GetInboxConversationMessages200ResponsePagination**](GetInboxConversationMessages200ResponsePagination.md)> |  | [optional]
**sort_order_applied** | Option<**SortOrderApplied**> | Sort order actually applied to the returned page. May differ from the requested `sortOrder` for Twitter, Facebook and Bluesky (always `desc` regardless of request).  (enum: asc, desc) | [optional]
**messages** | Option<[**Vec<models::GetInboxConversationMessages200ResponseMessagesInner>**](GetInboxConversationMessages200ResponseMessagesInner.md)> |  | [optional]
**last_updated** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


