# CreateAdCreativeRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token and Page. | 
**ad_account_id** | **String** | Platform ad account id (Meta act_<n>, Google customer id, LinkedIn account id, ...). | 
**headline** | **String** |  | 
**body** | **String** | Primary text | 
**description** | Option<**String**> | Link description below the headline; omitted = Meta scrapes the destination's OG description. | [optional]
**call_to_action** | Option<**String**> | CTA type (same whitelist as POST /v1/ads/create). | [optional][default to LEARN_MORE]
**link_url** | **String** |  | 
**image_url** | Option<**String**> | Publicly reachable image; uploaded to the account's library server-side. | [optional]
**image_hash** | Option<**String**> | Existing library image hash (POST /v1/ads/images or GET /v1/ads/images). | [optional]
**carousel_cards** | Option<[**Vec<models::CreateAdCreativeRequestCarouselCardsInner>**](CreateAdCreativeRequestCarouselCardsInner.md)> |  | [optional]
**url_tags** | Option<**String**> | Appended to every outbound URL (e.g. utm_source=fb). | [optional]
**promotion** | Option<**serde_json::Value**> | Not supported. Meta validates creative_sourcing_spec.promotion_metadata_spec on the create call and then discards it, so a Promotion set through the Marketing API never reaches the creative. Any object is rejected with 400 invalid_field_value. Send null or omit the field, and set the Promotion on the ad in Ads Manager. Verified on 2026-09-11 across Graph v19.0 to v25.0 and every write path. | [optional]
**creative_features** | Option<**std::collections::HashMap<String, Inner>**> | Meta only. Applied to each new creative, including standalone and attach shapes. With creatives[], these are defaults; an item replaces the whole feature map, including an empty map. auto_promotion_tag is an Advantage+ enhancement, not the Ads Manager Promotion setting. (enum: OPT_IN, OPT_OUT) | [optional]
**multi_advertiser** | Option<**MultiAdvertiser**> | Meta only. Multi-advertiser ads: whether Meta may show this ad alongside other advertisers' in one unit. Meta auto-enrols since Aug 2024, so send OPT_OUT to leave. It is a top-level creative field, NOT a `creativeFeatures` key, and Meta rejects it there. (enum: OPT_IN, OPT_OUT) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


