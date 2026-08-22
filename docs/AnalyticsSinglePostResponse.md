# AnalyticsSinglePostResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**post_id** | Option<**String**> |  | [optional]
**late_post_id** | Option<**String**> | Original Zernio post ID if scheduled via Zernio | [optional]
**status** | Option<**Status**> | Overall post status. \"partial\" when some platforms published and others failed. (enum: published, failed, partial) | [optional]
**content** | Option<**String**> |  | [optional]
**scheduled_for** | Option<**String**> |  | [optional]
**published_at** | Option<**String**> |  | [optional]
**analytics** | Option<[**models::PostAnalytics**](PostAnalytics.md)> |  | [optional]
**platform_analytics** | Option<[**Vec<models::PlatformAnalytics>**](PlatformAnalytics.md)> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**platform_post_url** | Option<**String**> |  | [optional]
**is_external** | Option<**bool**> |  | [optional]
**sync_status** | Option<**SyncStatus**> | Overall sync state across all platforms (enum: synced, pending, partial, unavailable) | [optional]
**message** | Option<**String**> | Human-readable status message for pending, partial, or failed states | [optional]
**thumbnail_url** | Option<**String**> |  | [optional]
**media_type** | Option<**MediaType**> |  (enum: image, video, carousel, text) | [optional]
**media_items** | Option<[**Vec<models::AnalyticsSinglePostResponseMediaItemsInner>**](AnalyticsSinglePostResponseMediaItemsInner.md)> | All media items for this post. Carousel posts contain one entry per slide. | [optional]
**media_product_type** | Option<**String**> | Instagram only: the platform media product type (e.g. FEED, REELS, STORY, AD). Absent when the platform did not report it. | [optional]
**is_ai_generated** | Option<**bool**> | Instagram only: whether Instagram labeled the media as AI-generated. Absent when the platform did not report it. | [optional]
**is_shared_to_feed** | Option<**bool**> | Instagram reels only: whether the reel is also shared to the main feed. Absent when the platform did not report it. | [optional]
**media_audio_type** | Option<**String**> | Instagram only: audio type of the media (MUSIC or ORIGINAL_SOUND). Absent when the platform did not report it. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


