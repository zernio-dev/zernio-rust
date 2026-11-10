# SearchInboxConversations200ResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accounts_queried** | Option<**i32**> |  | [optional]
**accounts_failed** | Option<**i32**> |  | [optional]
**failed_accounts** | Option<[**Vec<models::SearchInboxConversations200ResponseMetaFailedAccountsInner>**](SearchInboxConversations200ResponseMetaFailedAccountsInner.md)> |  | [optional]
**last_updated** | Option<**String**> |  | [optional]
**content_not_retained** | Option<**bool**> | True when a searched account belongs to a team that does not retain content. Message text is not searchable there, only identifiers match. | [optional]
**accounts_skipped** | Option<[**Vec<models::ListInboxConversations200ResponseMetaAccountsSkippedInner>**](ListInboxConversations200ResponseMetaAccountsSkippedInner.md)> | Connected messaging accounts that cannot be searched (live-fetched platforms) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


