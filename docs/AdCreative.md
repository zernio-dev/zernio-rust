# AdCreative

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**thumbnail_url** | Option<**String**> | Primary thumbnail/image URL | [optional]
**image_url** | Option<**String**> | Alternative image URL | [optional]
**video_id** | Option<**String**> | Meta video ID for VIDEO-type ads. Null for non-video ads. Callers that need an embeddable MP4 can call GET /{videoId}?fields=source with the page access token. | [optional]
**video_url** | Option<**String**> | Public Facebook watch URL for VIDEO-type ads (https://www.facebook.com/watch/?v={videoId}). Null for non-video ads. | [optional]
**creative_id** | Option<**String**> | Meta ad creative id backing this ad. Reusable via existingCreativeId on POST /v1/ads/create. | [optional]
**object_type** | Option<**String**> | Meta creative object_type (e.g. SHARE, VIDEO, PRIVACY_CHECK_FAIL, POST_DELETED). Use this to render state-aware previews — when Meta moderation strips image/video fields, only thumbnailUrl at 64x64 is available. | [optional]
**object_story_id** | Option<**String**> | Meta creative `object_story_id` (the SHARE reference). Frequently absent — Meta omits it for SHARE creatives. Use effectiveObjectStoryId instead. | [optional]
**effective_object_story_id** | Option<**String**> | Meta `effective_object_story_id` — `{pageId}_{postId}` of the Facebook post the ad's engagement (comments) lives on. Pass to GET /v1/ads?effectiveObjectStoryId= to map a Business-Manager-visible post back to this ad; GET /v1/ads/{adId}/comments resolves comments against it. | [optional]
**page_id** | Option<**String**> | Facebook Page backing the creative (Meta only). What the `pageId` filter on /v1/ads, /v1/ads/campaigns and /v1/ads/tree matches against. Absent for non-Meta ads and rare Meta creatives with no page signal. | [optional]
**effective_instagram_media_id** | Option<**String**> | Meta `effective_instagram_media_id` — the Instagram media ID of the boosted post the ad's engagement lives on. Pass to GET /v1/ads?effectiveInstagramMediaId= to map a Business-Manager-visible IG post back to this ad. | [optional]
**instagram_user_id** | Option<**String**> | Meta `instagram_user_id` — the Instagram-scoped business ID that owns the boosted media. | [optional]
**instagram_permalink_url** | Option<**String**> | Meta `instagram_permalink_url` — public Instagram post URL of the boosted media. | [optional]
**media_urls** | Option<**Vec<String>**> | All media URLs for this ad (carousel images, multiple assets). Populated for Meta (carousel child_attachments), Google Ads (responsive display marketing_images), and LinkedIn (multi-image posts). | [optional]
**is_serving** | Option<**bool**> | LinkedIn only. Whether LinkedIn is currently serving this specific creative. Complements the ad-level `servingStatuses`, which describes the parent campaign. | [optional]
**serving_hold_reasons** | Option<**Vec<String>**> | LinkedIn only. Why this specific creative is not being served. Empty when it is serving. A superset of the ad-level `servingStatuses`: it repeats the inherited campaign, campaign group and account holds AND adds creative-only causes such as UNDER_REVIEW, REJECTED, PROCESSING, PROCESSING_FAILED, FORM_HOLD (lead-gen-form creatives), REFERRED_CONTENT_QUALITY_HOLD, JOB_POSTING_ON_HOLD and JOB_POSTING_INVALID (job ads). Some values are format-specific and will never appear on other ad formats. The list is open, so treat unrecognized values as holds rather than errors.  | [optional]
**body** | Option<**String**> | Ad copy/text | [optional]
**google_headline** | Option<**String**> | Google Ads headline | [optional]
**google_description** | Option<**String**> | Google Ads description | [optional]
**link_url** | Option<**String**> | Destination URL | [optional]
**pinterest_image_url** | Option<**String**> |  | [optional]
**pinterest_title** | Option<**String**> |  | [optional]
**pinterest_description** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


