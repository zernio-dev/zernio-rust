# PostMetricRow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**date** | Option<**String**> | The day, with granularity=day. | [optional]
**post_id** | Option<**String**> | The Zernio post, null for a post published outside Zernio. | 
**external_post_id** | Option<**String**> | The synced post, null while a published post waits for its first sync. | 
**account_id** | **String** |  | 
**profile_id** | Option<**String**> |  | 
**platform** | **String** |  | 
**platform_post_id** | Option<**String**> |  | 
**platform_post_url** | Option<**String**> |  | 
**published_at** | Option<**String**> |  | 
**last_synced_at** | Option<**String**> |  | 
**sync_status** | **SyncStatus** |  (enum: synced, pending, unavailable) | 
**sync_error** | Option<[**models::PostMetricRowSyncError**](PostMetricRowSyncError.md)> |  | 
**is_owner** | Option<**bool**> |  | 
**is_ad** | Option<**bool**> |  | 
**metrics** | **std::collections::HashMap<String, f64>** | Each metric asked; null when the platform does not report it or no snapshot exists yet. | 
**breakdowns** | Option<[**std::collections::HashMap<String, models::PostMetricRowBreakdownsValue>**](PostMetricRowBreakdownsValue.md)> |  | [optional]
**post** | Option<[**models::PostMetricContent**](PostMetricContent.md)> |  | [optional]
**authenticity** | Option<[**models::PostMetricAuthenticity**](PostMetricAuthenticity.md)> |  | [optional]
**samples** | Option<[**Vec<models::PostMetricSample>**](PostMetricSample.md)> | With include=samples: the readings of the publication, oldest first. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


