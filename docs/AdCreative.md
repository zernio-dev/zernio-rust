# AdCreative

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**asset_group** | Option<[**models::GooglePmaxAssetGroupInput**](GooglePmaxAssetGroupInput.md)> | Initial Performance Max asset group input. Use the asset-groups endpoint for current Google assets. | [optional]
**asset_group_resource_name** | Option<**String**> | Google resource name of the created Performance Max asset group. | [optional]
**headlines** | Option<[**Vec<models::AdCreativeHeadlinesInner>**](AdCreativeHeadlinesInner.md)> | Google RSA: the headline assets as objects (3 to 15). Meta: every title variation of the creative (`asset_feed_spec.titles`) as strings, the same shape as the `headlines` create input. Present only with 2 or more titles; a single title is `headline`. | [optional]
**descriptions** | Option<[**Vec<models::AdCreativeDescriptionsInner>**](AdCreativeDescriptionsInner.md)> | Google RSA: the description assets as objects (2 to 4). Meta: every description variation of the creative (`asset_feed_spec.descriptions`) as strings, the same shape as the `descriptions` create input. Present only with 2 or more descriptions; a single one is `description`. | [optional]
**headline** | Option<**String**> | Meta: the creative's title (`link_data.name`, `video_data.title`, or the first `asset_feed_spec.titles` entry). Absent when the creative has none. | [optional]
**bodies** | Option<**Vec<String>**> | Meta: every primary text variation of the creative (`asset_feed_spec.bodies`), the same shape as the `bodies` create input. Present only with 2 or more texts; a single text is `body`. | [optional]
**description** | Option<**String**> | Meta: the creative's description under the title (`link_data.description`, `video_data.link_description`, or the first `asset_feed_spec.descriptions` entry). | [optional]
**call_to_action** | Option<**String**> | Meta: the call to action type (`call_to_action.type`, or the first `asset_feed_spec.call_to_action_types` entry), e.g. LEARN_MORE or SIGN_UP. | [optional]
**lead_gen_form_id** | Option<**String**> | Meta: the instant form the call to action opens (`call_to_action.value.lead_gen_form_id`), the same value as the `leadGenFormId` create input. Absent on ads without a lead form. | [optional]
**image_hash** | Option<**String**> | Meta: the ad image hash (`image_hash`), reusable as `imageHash` on POST /v1/ads/create within the same ad account. `thumbnailUrl` and `mediaUrls` carry its stable full resolution permalink when Meta resolves it. | [optional]
**url_tags** | Option<**String**> | Meta: the creative's `url_tags` query string appended to the destination URL. | [optional]
**final_urls** | Option<**Vec<String>**> | Google RSA only. Replaces final URLs. Omitted lists stay unchanged. | [optional]
**thumbnail_url** | Option<**String**> | Primary thumbnail/image URL | [optional]
**image_url** | Option<**String**> | Alternative image URL | [optional]
**asset_resource_name** | Option<**String**> | Google Display only. Resource name of the landscape marketing image asset (`creative.imageUrl`), for example customers/1234567890/assets/123. Set at creation and updated when PUT /v1/ads/{adId} replaces `creative.imageUrl`; replacing only `creative.squareImageUrl` leaves it unchanged. | [optional]
**assets** | Option<[**models::AdCreativeAssets**](AdCreativeAssets.md)> |  | [optional]
**video_id** | Option<**String**> | Meta video ID for VIDEO-type ads. Null for non-video ads. Callers that need an embeddable MP4 can call GET /{videoId}?fields=source with the page access token. | [optional]
**video_url** | Option<**String**> | Public Facebook watch URL for VIDEO-type ads (https://www.facebook.com/watch/?v={videoId}). Null for non-video ads. | [optional]
**creative_id** | Option<**String**> | Meta ad creative id backing this ad, refreshed from Meta on every sync. Reusable via existingCreativeId on POST /v1/ads/create, and readable raw through GET /v1/ads/creatives/{creativeId}. Ads synced from Meta also carry it as the legacy `id` key. | [optional]
**creative_features** | Option<**std::collections::HashMap<String, Inner>**> | Meta only. The creativeFeatures map sent at creation (degrees_of_freedom_spec.creative_features_spec). Absent on ads synced from Meta. (enum: OPT_IN, OPT_OUT) | [optional]
**catalog** | Option<[**models::AdCreativeCatalog**](AdCreativeCatalog.md)> |  | [optional]
**object_type** | Option<**String**> | Meta creative object_type (e.g. SHARE, VIDEO, PRIVACY_CHECK_FAIL, POST_DELETED). Use this to render state-aware previews: when Meta moderation strips image/video fields, only thumbnailUrl at 64x64 is available. | [optional]
**object_story_id** | Option<**String**> | Meta creative `object_story_id` (the SHARE reference). Frequently absent, because Meta omits it for SHARE creatives. Use effectiveObjectStoryId instead. | [optional]
**effective_object_story_id** | Option<**String**> | Meta `effective_object_story_id`, the `{pageId}_{postId}` of the Facebook post the ad's engagement (comments) lives on. Pass to GET /v1/ads?effectiveObjectStoryId= to map a Business-Manager-visible post back to this ad; GET /v1/ads/{adId}/comments resolves comments against it. | [optional]
**page_id** | Option<**String**> | Facebook Page backing the creative (Meta only). What the `pageId` filter on /v1/ads, /v1/ads/campaigns and /v1/ads/tree matches against. Absent for non-Meta ads and rare Meta creatives with no page signal. | [optional]
**effective_instagram_media_id** | Option<**String**> | Meta `effective_instagram_media_id`, the Instagram media ID of the boosted post the ad's engagement lives on. Pass to GET /v1/ads?effectiveInstagramMediaId= to map a Business-Manager-visible IG post back to this ad. | [optional]
**instagram_user_id** | Option<**String**> | Meta `instagram_user_id`, the Instagram-scoped business ID that owns the boosted media. | [optional]
**instagram_permalink_url** | Option<**String**> | Meta `instagram_permalink_url`, the public Instagram post URL of the boosted media. | [optional]
**media_urls** | Option<**Vec<String>**> | All media URLs for this ad (carousel images, multiple assets). Populated for Meta (carousel child_attachments), Google Ads (responsive display marketing_images), and LinkedIn (multi-image posts). | [optional]
**carousel_cards** | Option<[**Vec<models::AdCreativeCarouselCardsInner>**](AdCreativeCarouselCardsInner.md)> | Meta only today. The carousel's cards in display order, one per Meta `link_data.child_attachments` entry, using the same field names as the `carouselCards` create input. Absent on non-carousel ads and other platforms.  - Synced from Meta: `imageUrl` is resolved exactly like `mediaUrls` (the stable `/adimages` permalink first), so cards with an image line up with `mediaUrls` in order. A card whose image Meta does not resolve keeps its place without `imageUrl`. - Created through Zernio: starts as the cards you sent. - Synced carousels stored before this field existed fill it in on their next sync.  | [optional]
**is_serving** | Option<**bool**> | LinkedIn only. Whether LinkedIn is currently serving this specific creative. Complements the ad-level `servingStatuses`, which describes the parent campaign. | [optional]
**ad_format** | Option<**String**> | LinkedIn only. The LinkedIn ad format, in LinkedIn's own vocabulary: STANDARD_UPDATE, SINGLE_VIDEO, CAROUSEL, NATIVE_DOCUMENT, EVENT, TEXT_AD, SPOTLIGHT, FOLLOW_COMPANY, JOBS, SPONSORED_INMAILS and others. The list is open, so treat an unrecognized value as valid.  - On an ad Zernio created: the format it was created as. - On an ad synced from Campaign Manager: the parent campaign's raw `format`, which is what LinkedIn actually enforces on its creatives.  Absent on LinkedIn ads not yet re-synced, and on every other platform. | [optional]
**serving_hold_reasons** | Option<**Vec<String>**> | LinkedIn only. Why this specific creative is not being served. Empty when it is serving.  A superset of the ad-level `servingStatuses`: it repeats the inherited campaign, campaign group and account holds AND adds creative-only causes, such as:  - UNDER_REVIEW, REJECTED, PROCESSING, PROCESSING_FAILED; - FORM_HOLD (lead-gen-form creatives); - REFERRED_CONTENT_QUALITY_HOLD; - JOB_POSTING_ON_HOLD and JOB_POSTING_INVALID (job ads).  Some values are format-specific and will never appear on other ad formats. The list is open, so treat unrecognized values as holds rather than errors.  | [optional]
**body** | Option<**String**> | Ad copy/text | [optional]
**google_headline** | Option<**String**> | Google Ads headline | [optional]
**google_description** | Option<**String**> | Google Ads description | [optional]
**youtube_video_ids** | Option<**Vec<String>**> | Google only. YouTube video ids behind a Video campaign ad (video and responsive video ads) or a Demand Gen video ad, same id as `youtubeVideoId` on Performance Max asset groups. When the ad has no image, `thumbnailUrl` is the first video's YouTube thumbnail. Absent on ads without a video. | [optional]
**link_url** | Option<**String**> | Destination URL | [optional]
**whatsapp_phone_number** | Option<**String**> | Explicit E.164 WhatsApp number supplied when creating a Meta boost or messaging ad. Absent when omitted by the caller or on older records. | [optional]
**instagram_video_fallback** | Option<[**models::InstagramVideoFallback**](InstagramVideoFallback.md)> |  | [optional]
**pinterest_image_url** | Option<**String**> |  | [optional]
**pinterest_title** | Option<**String**> |  | [optional]
**pinterest_description** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


