# FacebookPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**draft** | Option<**bool**> | When true, creates the post as an unpublished draft visible in Facebook Publishing Tools instead of publishing immediately. Supported for feed posts (text, link, image, video) and reels. Not supported for stories. Drafts expire after ~30 days. | [optional][default to false]
**content_type** | Option<**ContentType**> | Set to 'story' for Page Stories (24h ephemeral) or 'reel' for Reels (short vertical video). Defaults to feed post if omitted. (enum: story, reel) | [optional]
**title** | Option<**String**> | Reel title (only for contentType=reel). Separate from the caption/content field. | [optional]
**first_comment** | Option<**String**> | Optional first comment to post immediately after publishing (feed posts and reels, not stories). Skipped when draft is true. | [optional]
**page_id** | Option<**String**> | Target Facebook Page ID for multi-page posting. If omitted, uses the default page. Use GET /v1/accounts/{id}/facebook-page to list pages. | [optional]
**geo_restriction** | Option<[**models::GeoRestriction**](GeoRestriction.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


