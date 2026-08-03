# UpdatePostRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | Option<**String**> |  | [optional]
**content** | Option<**String**> |  | [optional]
**media_items** | Option<[**Vec<models::MediaItem>**](MediaItem.md)> |  | [optional]
**platforms** | Option<[**Vec<models::UpdatePostRequestPlatformsInner>**](UpdatePostRequestPlatformsInner.md)> | Target platforms and accounts for this post. Each item must include platform and accountId. | [optional]
**scheduled_for** | Option<**String**> |  | [optional]
**publish_now** | Option<**bool**> |  | [optional][default to false]
**is_draft** | Option<**bool**> | When omitted, the post keeps its current draft status. Send `false` to promote a draft to scheduled (combined with `scheduledFor`, `publishNow`, or a queue). | [optional]
**timezone** | Option<**String**> |  | [optional]
**visibility** | Option<**Visibility**> |  (enum: public, private, unlisted) | [optional]
**tags** | Option<**Vec<String>**> |  | [optional]
**hashtags** | Option<**Vec<String>**> |  | [optional]
**mentions** | Option<**Vec<String>**> |  | [optional]
**crossposting_enabled** | Option<**bool**> |  | [optional]
**metadata** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]
**queued_from_profile** | Option<**String**> | Profile ID to schedule via queue. | [optional]
**queue_id** | Option<**String**> | Specific queue ID to use when scheduling via queue. | [optional]
**tiktok_settings** | Option<[**models::TikTokPlatformData**](TikTokPlatformData.md)> | Root-level TikTok settings applied to the TikTok platforms sent in the same request. Merged into each platform's platformSpecificData, with platform-specific settings taking precedence. Returns 400 if sent without a platforms array. | [optional]
**facebook_settings** | Option<[**models::FacebookSettings**](FacebookSettings.md)> | Root-level Facebook settings applied to the Facebook platforms sent in the same request. Merged into each platform's platformSpecificData.facebookSettings, with platform-specific settings taking precedence. Returns 400 if sent without a platforms array. | [optional]
**recycling** | Option<[**models::RecyclingConfig**](RecyclingConfig.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


