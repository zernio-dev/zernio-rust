# ListInboxComments200ResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accounts_queried** | Option<**i32**> |  | [optional]
**accounts_failed** | Option<**i32**> |  | [optional]
**failed_accounts** | Option<[**Vec<models::ListInboxComments200ResponseMetaFailedAccountsInner>**](ListInboxComments200ResponseMetaFailedAccountsInner.md)> |  | [optional]
**last_updated** | Option<**String**> |  | [optional]
**accounts_skipped** | Option<[**Vec<models::ListInboxConversations200ResponseMetaAccountsSkippedInner>**](ListInboxConversations200ResponseMetaAccountsSkippedInner.md)> | Connected accounts that were not queried: their platform does not support this feature, or the account is not enabled for it | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


