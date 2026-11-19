# PostMetricsResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**date** | Option<**String**> | The day, with granularity=day. | [optional]
**post_id** | **String** |  | 
**external_post_id** | **String** |  | 
**account_id** | **String** |  | 
**profile_id** | **String** |  | 
**platform** | **String** |  | 
**platform_post_id** | **String** |  | 
**platform_post_url** | **String** |  | 
**published_at** | **String** |  | 
**last_synced_at** | **String** |  | 
**sync_status** | **SyncStatus** |  (enum: synced, pending, unavailable) | 
**sync_error** | Option<[**models::PostMetricRowSyncError**](PostMetricRowSyncError.md)> |  | 
**is_owner** | **bool** |  | 
**is_ad** | **bool** |  | 
**metrics** | **std::collections::HashMap<String, f64>** | Each metric asked, as the platform reported it in this change; null when the post's platform does not report it. | 
**breakdowns** | Option<[**std::collections::HashMap<String, models::PostMetricRowBreakdownsValue>**](PostMetricRowBreakdownsValue.md)> |  | [optional]
**post** | Option<[**models::PostMetricContent**](PostMetricContent.md)> |  | [optional]
**authenticity** | Option<[**models::PostMetricAuthenticity**](PostMetricAuthenticity.md)> |  | [optional]
**samples** | Option<[**Vec<models::PostMetricSample>**](PostMetricSample.md)> | With include=samples: the readings of the publication, oldest first. | [optional]
**platforms** | **Vec<String>** |  | 
**account_ids** | **Vec<String>** |  | 
**publications** | **i32** |  | 
**day_of_week** | **i32** | UTC weekday the posts were published, 1 (Monday) to 7. | 
**hour** | **i32** | UTC hour the posts were published, 0 to 23. | 
**post_count** | **i32** | Posts of the format published in the range. | 
**post_age** | **String** | Time since publishing: 0-6h, 6-12h, 12-24h, 1-2d, 2-7d, 7-30d or 30d+. | 
**format** | **Format** | gif counts as image, document as text. (enum: image, video, carousel, text) | 
**synced_at** | **String** | When the account's sync cycle that read these numbers started. Not an order: resume with the cursor only. | 
**deleted** | **bool** | True when the post was removed from the platform. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


