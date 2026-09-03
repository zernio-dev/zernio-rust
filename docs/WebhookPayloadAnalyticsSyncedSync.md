# WebhookPayloadAnalyticsSyncedSync

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**synced_at** | **String** | When the cycle COMPLETED. Not a join key for the delta feed: the rows a cycle produces carry a `syncedAt` stamped when the cycle STARTED, which is measured at around one second earlier at the median and up to a couple of minutes earlier in the tail. Correlate on `account.accountId`.  | 
**posts_updated** | **i32** | Post records created or modified by this cycle. Not the number of delta feed rows the cycle produced, which the syncer does not report, so a cycle with a non-zero `postsUpdated` can still yield an empty delta page.  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


