# GetInboxTopAccounts200ResponseAccountsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**display_name** | Option<**String**> | (disconnected) when the SocialAccount no longer exists | [optional]
**username** | Option<**String**> |  | [optional]
**received** | Option<**i32**> |  | [optional]
**sent** | Option<**i32**> |  | [optional]
**total** | Option<**i32**> |  | [optional]
**conversations** | Option<**i32**> |  | [optional]
**median_response_seconds** | Option<**i32**> |  | [optional]
**replied_count** | Option<**i32**> | Distinguishes 'instant replies' from 'no replies at all' so a zero medianResponseSeconds with repliedCount=0 renders as '—' instead of '0s' | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


