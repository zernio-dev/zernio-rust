# ExternalPostSummary

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | Option<**String**> | Platform the post belongs to (e.g. instagram, youtube, tiktok) | [optional]
**platform_post_id** | Option<**String**> | The platform's own post/media/video id | [optional]
**platform_post_url** | Option<**String**> | Canonical URL (permalink) of the post on the platform | [optional]
**content** | Option<**String**> | Post caption / text | [optional]
**published_at** | Option<**String**> | When the post was published on the platform | [optional]
**media_type** | Option<**String**> | Media type (e.g. image, video, carousel) | [optional]
**thumbnail_url** | Option<**String**> | Thumbnail URL | [optional]
**media_items** | Option<**Vec<serde_json::Value>**> | Per-item media (for carousels / multi-media posts) | [optional]
**media_product_type** | Option<**String**> | Instagram only: the platform media product type (e.g. FEED, REELS, STORY, AD). Absent when the platform did not report it. | [optional]
**is_ai_generated** | Option<**bool**> | Instagram only: whether Instagram labeled the media as AI-generated. Absent when the platform did not report it. | [optional]
**is_shared_to_feed** | Option<**bool**> | Instagram reels only: whether the reel is also shared to the main feed. Absent when the platform did not report it. | [optional]
**media_audio_type** | Option<**String**> | Instagram only: audio type of the media (MUSIC or ORIGINAL_SOUND). Absent when the platform did not report it. | [optional]
**analytics** | Option<[**models::ExternalPostSummaryAnalytics**](ExternalPostSummaryAnalytics.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


