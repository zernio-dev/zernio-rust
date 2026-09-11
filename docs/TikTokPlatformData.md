# TikTokPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**draft** | Option<**bool**> | When true, sends the post to the TikTok Creator Inbox as a draft instead of publishing immediately. The creator receives an inbox notification to complete posting via TikTok's editing flow. Maps to TikTok API post_mode: \"MEDIA_UPLOAD\" (photos) or the dedicated inbox endpoint (videos). When false or omitted, publishes directly via post_mode: \"DIRECT_POST\". Note: publish_type is not a supported field. Use this field instead.  | [optional]
**privacy_level** | Option<**String**> | One of the values returned by the TikTok creator info API for the account. Accounts connected through the TikTok for Business app publish videos as public only: a non-public value on a video post is rejected at creation unless draft is true (photo posts keep every level). | [optional]
**allow_comment** | Option<**bool**> | Allow comments on the post | [optional]
**allow_duet** | Option<**bool**> | Allow duets (required for video posts) | [optional]
**allow_stitch** | Option<**bool**> | Allow stitches (required for video posts) | [optional]
**commercial_content_type** | Option<**CommercialContentType**> | Type of commercial content disclosure. Sufficient on its own: \"brand_organic\" (\"Your Brand\") implies isBrandOrganicPost and \"brand_content\" (\"Branded Content\", paid partnership) implies brandPartnerPromote, so you don't need to send the boolean flags separately. Branded content cannot be posted with privacyLevel SELF_ONLY.  (enum: none, brand_organic, brand_content) | [optional]
**brand_partner_promote** | Option<**bool**> | Whether the post promotes a brand partner (branded content / paid partnership). Only needed to disclose BOTH types at once (set it alongside commercialContentType \"brand_organic\"), or to override the value implied by commercialContentType.  | [optional]
**is_brand_organic_post** | Option<**bool**> | Whether the post promotes the creator's own brand (brand organic). Only needed to disclose BOTH types at once (set it alongside commercialContentType \"brand_content\"), or to override the value implied by commercialContentType.  | [optional]
**content_preview_confirmed** | Option<**bool**> | User has confirmed they previewed the content | [optional]
**express_consent_given** | Option<**bool**> | User has given express consent for posting | [optional]
**media_type** | Option<**MediaType**> | Optional override. Defaults based on provided media items. (enum: video, photo) | [optional]
**video_cover_timestamp_ms** | Option<**i32**> | Optional for video posts. Timestamp in milliseconds to select which frame to use as thumbnail (defaults to 1000ms/1 second). Ignored when videoCoverImageUrl is provided. | [optional]
**video_cover_image_url** | Option<**String**> | Optional for video posts. URL of a custom thumbnail image (JPG, PNG, or WebP, max 20MB). The image is stitched as a single frame at the start of the video and used as the cover. Accounts connected through the TikTok for Business app instead pass the URL to TikTok as the cover directly, with no stitching, and the URL must resolve on a domain we have verified with TikTok. Overrides videoCoverTimestampMs when provided. | [optional]
**photo_cover_index** | Option<**i32**> | Optional for photo carousels. Index of image to use as cover, 0-based (defaults to 0/first image). | [optional]
**auto_add_music** | Option<**bool**> | When true, TikTok may add recommended music (photos only) | [optional]
**video_made_with_ai** | Option<**bool**> | Set true to disclose AI-generated content. Accounts connected through the TikTok for Business app carry the disclosure on video posts only: the business photo endpoint has no AI disclosure field, so true on a direct photo post is rejected at creation rather than published undisclosed. Send draft true to publish such a photo post and set the disclosure in the TikTok app. | [optional]
**description** | Option<**String**> | Optional long-form caption for photo posts (max 4000 chars). Recommended when content exceeds 90 chars, as photo titles are auto-truncated. Falls back to the post content when omitted. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


