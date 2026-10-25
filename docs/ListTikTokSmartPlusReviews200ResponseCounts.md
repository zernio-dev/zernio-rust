# ListTikTokSmartPlusReviews200ResponseCounts

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fresh** | Option<**i32**> | Items read within `maxAgeSeconds`. | [optional]
**stale** | Option<**i32**> | Items read earlier, returned with their `readAt` and due for a refresh. | [optional]
**pending** | Option<**i32**> | Smart+ ads never read (`pendingSmartPlusAdIds`). | [optional]
**failed** | Option<**i32**> | Entries of `failedSmartPlusAds`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


