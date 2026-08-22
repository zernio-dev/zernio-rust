# ExternalPostWebhookPost

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Platform-native post ID (NOT a Zernio post ID). | 
**platform** | **String** | Platform the post lives on (e.g. \"googlebusiness\"). | 
**account_id** | **String** | Zernio social account ID the post belongs to. | 
**url** | Option<**String**> | Direct URL to the post on the platform, when available. | 
**content** | **String** | Post text. May be empty. | 
**media_type** | **String** | One of image, video, gif, document, text, carousel. | 
**media_items** | [**Vec<models::ExternalPostMediaItem>**](ExternalPostMediaItem.md) |  | 
**thumbnail_url** | Option<**String**> |  | 
**published_at** | **String** |  | 
**media_product_type** | Option<**String**> | Instagram only: the platform media product type (e.g. FEED, REELS, STORY, AD). Absent when the platform did not report it. | [optional]
**is_ai_generated** | Option<**bool**> | Instagram only: whether Instagram labeled the media as AI-generated. Absent when the platform did not report it. | [optional]
**is_shared_to_feed** | Option<**bool**> | Instagram reels only: whether the reel is also shared to the main feed. Absent when the platform did not report it. | [optional]
**media_audio_type** | Option<**String**> | Instagram only: audio type of the media (MUSIC or ORIGINAL_SOUND). Absent when the platform did not report it. | [optional]
**source** | **Source** | Always \"external\" — distinguishes these from Zernio-originated post.* events. (enum: external) | 
**deleted_at** | Option<**String**> | Detection time of deletion. Present on post.external.deleted; null/absent otherwise. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


