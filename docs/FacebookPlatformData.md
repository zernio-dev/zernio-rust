# FacebookPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content_type** | Option<**ContentType**> | Set to 'story' for Page Stories (24h ephemeral) or 'reel' for Reels (short vertical video). Defaults to feed post if omitted. (enum: story, reel) | [optional]
**title** | Option<**String**> | Reel title (only for contentType=reel). Separate from the caption/content field. | [optional]
**first_comment** | Option<**String**> | Optional first comment to post immediately after publishing (feed posts and reels, not stories). Skipped when facebookSettings.draft is true. | [optional]
**is_ai_generated** | Option<**bool**> | When true, Facebook shows its AI-disclosure label on the post. Forwarded as is_ai_generated on Reels (contentType=reel) and video Stories (contentType=story with a video). Meta documents no such parameter for feed posts, feed videos or photo Stories, so the flag is accepted with a warning and no label there. | [optional][default to false]
**page_id** | Option<**String**> | Target Facebook Page ID for multi-page posting. If omitted, uses the default page. Use GET /v1/accounts/{id}/facebook-page to list pages. | [optional]
**geo_restriction** | Option<[**models::GeoRestriction**](GeoRestriction.md)> |  | [optional]
**facebook_settings** | Option<[**models::FacebookSettings**](FacebookSettings.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


