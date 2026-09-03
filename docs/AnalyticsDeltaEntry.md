# AnalyticsDeltaEntry

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**post_id** | **String** | External post ID. The same identifier as `posts[]._id` in GET /v1/analytics. | 
**account_id** | **String** | Social account this post was published through | 
**profile_id** | **String** | Profile the account belongs to | 
**platform** | **String** |  | 
**platform_post_id** | **String** | Platform-side post ID (for example the YouTube video ID) | 
**published_at** | **String** | When the post was published, ISO-8601 UTC | 
**synced_at** | **String** | When the sync cycle that produced this snapshot STARTED, ISO-8601 UTC. This is NOT the order entries arrive in and it is not a resume point: a slow cycle writes its rows after a faster cycle that started later, so `syncedAt` can go backwards between consecutive entries. Use `nextCursor` to resume.  | 
**is_deleted** | **bool** | True when the post was detected as deleted on the platform at this sync | 
**metrics** | [**models::AnalyticsDeltaEntryMetrics**](AnalyticsDeltaEntryMetrics.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


