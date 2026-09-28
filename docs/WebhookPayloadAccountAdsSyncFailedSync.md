# WebhookPayloadAccountAdsSyncFailedSync

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**last_successful_sync_at** | **String** |  | 
**failure_count** | **i32** | Consecutive failed sync attempts on the ad account's ads. | 
**error_category** | **ErrorCategory** | ad_account_not_listed = the platform no longer returns the ad account to this connection (access removed, or a platform-side change); sync_error = the platform returned an error, see `error`; stale = no sync succeeded and no error was recorded. New values may be added.  (enum: ad_account_not_listed, sync_error, stale) | 
**error** | **String** | Human-readable detail, for display and debugging. Branch on errorCategory. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


