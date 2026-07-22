# CreateAdCreativeRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token and Page. | 
**ad_account_id** | **String** | Meta ad account id (act_<n>). | 
**headline** | **String** |  | 
**body** | **String** | Primary text | 
**description** | Option<**String**> | Link description below the headline; omitted = Meta scrapes the destination's OG description. | [optional]
**call_to_action** | Option<**String**> | CTA type (same whitelist as POST /v1/ads/create). | [optional][default to LEARN_MORE]
**link_url** | **String** |  | 
**image_url** | Option<**String**> | Publicly reachable image; uploaded to the account's library server-side. | [optional]
**image_hash** | Option<**String**> | Existing library image hash (POST /v1/ads/images or GET /v1/ads/images). | [optional]
**carousel_cards** | Option<[**Vec<models::CreateAdCreativeRequestCarouselCardsInner>**](CreateAdCreativeRequestCarouselCardsInner.md)> |  | [optional]
**url_tags** | Option<**String**> | Appended to every outbound URL (e.g. utm_source=fb). | [optional]
**creative_features** | Option<**std::collections::HashMap<String, Inner>**> | Advantage+ creative enhancements: partial map of Meta creative feature keys (snake_case) to enroll status, forwarded as degrees_of_freedom_spec.creative_features_spec. Unspecified features default to OPT_OUT. (enum: OPT_IN, OPT_OUT) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


