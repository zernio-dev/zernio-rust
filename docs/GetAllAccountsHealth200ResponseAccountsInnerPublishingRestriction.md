# GetAllAccountsHealth200ResponseAccountsInnerPublishingRestriction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**reason** | Option<**Reason**> |  (enum: restricted, suspended, verification_required, auth_expired) | [optional]
**message** | Option<**String**> | The stored error message of the last failed publish. | [optional]
**since** | Option<**String**> |  | [optional]
**last_failed_at** | Option<**String**> |  | [optional]
**blocks_publish_now** | Option<**bool**> | True while POST /v1/posts refuses publish-now posts to this account with 422 `account_restricted` (24 hours after the last failure). Scheduled posts are always accepted. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


