# AnalyticsListResponsePostsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**late_post_id** | Option<**String**> | Original Zernio post ID if scheduled via Zernio | [optional]
**content** | Option<**String**> |  | [optional]
**scheduled_for** | Option<**String**> |  | [optional]
**published_at** | Option<**String**> |  | [optional]
**status** | Option<**String**> |  | [optional]
**analytics** | Option<[**models::PostAnalytics**](PostAnalytics.md)> |  | [optional]
**platforms** | Option<[**Vec<models::PlatformAnalytics>**](PlatformAnalytics.md)> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**platform_post_url** | Option<**String**> |  | [optional]
**is_external** | Option<**bool**> |  | [optional]
**is_ad** | Option<**bool**> | True when this post's metrics include paid delivery, so organic reporting should exclude it. Set for LinkedIn dark posts and for TikTok posts that one of your TikTok ads promotes (Spark / boosted). TikTok exposes no ad flag of its own, so a video created by an uploaded-asset (non-Spark) TikTok ad is posted to the profile with a fresh organic id and cannot be detected: those still report as false. | [optional]
**profile_id** | Option<**String**> |  | [optional]
**thumbnail_url** | Option<**String**> | Cover image URL. Facebook and Instagram covers whose Meta CDN link expired are re-read from Meta and served from Zernio storage, so that URL does not expire and can be cached. | [optional]
**media_type** | Option<**MediaType**> |  (enum: image, video, gif, document, carousel, text) | [optional]
**media_items** | Option<[**Vec<models::AnalyticsListResponsePostsInnerMediaItemsInner>**](AnalyticsListResponsePostsInnerMediaItemsInner.md)> | All media items for this post. Carousel posts contain one entry per slide. Facebook and Instagram images and video covers whose Meta CDN links expired are re-read and served from Zernio storage (non-expiring). Facebook and Instagram video file URLs, and LinkedIn media URLs, stay the platform's signed links and are refreshed on read once they lapse. | [optional]
**media_product_type** | Option<**String**> | Instagram only: the platform media product type (e.g. FEED, REELS, STORY, AD). Absent when the platform did not report it. | [optional]
**is_ai_generated** | Option<**bool**> | Instagram only: whether Instagram labeled the media as AI-generated. Absent when the platform did not report it. | [optional]
**is_shared_to_feed** | Option<**bool**> | Instagram reels only: whether the reel is also shared to the main feed. Absent when the platform did not report it. | [optional]
**media_audio_type** | Option<**String**> | Instagram only: audio type of the media (MUSIC or ORIGINAL_SOUND). Absent when the platform did not report it. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


