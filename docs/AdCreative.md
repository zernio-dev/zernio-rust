# AdCreative

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**thumbnail_url** | Option<**String**> | Primary thumbnail/image URL | [optional]
**image_url** | Option<**String**> | Alternative image URL | [optional]
**video_id** | Option<**String**> | Meta video ID for VIDEO-type ads. Null for non-video ads. Callers that need an embeddable MP4 can call GET /{videoId}?fields=source with the page access token. | [optional]
**video_url** | Option<**String**> | Public Facebook watch URL for VIDEO-type ads (https://www.facebook.com/watch/?v={videoId}). Null for non-video ads. | [optional]
**object_type** | Option<**String**> | Meta creative object_type (e.g. SHARE, VIDEO, PRIVACY_CHECK_FAIL, POST_DELETED). Use this to render state-aware previews — when Meta moderation strips image/video fields, only thumbnailUrl at 64x64 is available. | [optional]
**object_story_id** | Option<**String**> | Meta creative `object_story_id` (the SHARE reference). Frequently absent — Meta omits it for SHARE creatives. Use effectiveObjectStoryId instead. | [optional]
**effective_object_story_id** | Option<**String**> | Meta `effective_object_story_id` — `{pageId}_{postId}` of the Facebook post the ad's engagement (comments) lives on. Pass to GET /v1/ads?effectiveObjectStoryId= to map a Business-Manager-visible post back to this ad; GET /v1/ads/{adId}/comments resolves comments against it. | [optional]
**effective_instagram_media_id** | Option<**String**> | Meta `effective_instagram_media_id` — the Instagram media ID of the boosted post the ad's engagement lives on. Pass to GET /v1/ads?effectiveInstagramMediaId= to map a Business-Manager-visible IG post back to this ad. | [optional]
**instagram_user_id** | Option<**String**> | Meta `instagram_user_id` — the Instagram-scoped business ID that owns the boosted media. | [optional]
**instagram_permalink_url** | Option<**String**> | Meta `instagram_permalink_url` — public Instagram post URL of the boosted media. | [optional]
**media_urls** | Option<**Vec<String>**> | All media URLs for this ad (carousel images, multiple assets). Populated for Meta (carousel child_attachments), Google Ads (responsive display marketing_images), and LinkedIn (multi-image posts). | [optional]
**body** | Option<**String**> | Ad copy/text | [optional]
**google_headline** | Option<**String**> | Google Ads headline | [optional]
**google_description** | Option<**String**> | Google Ads description | [optional]
**link_url** | Option<**String**> | Destination URL | [optional]
**pinterest_image_url** | Option<**String**> |  | [optional]
**pinterest_title** | Option<**String**> |  | [optional]
**pinterest_description** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


