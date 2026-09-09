# UpdateAdRequestCreative

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**promotion** | Option<[**models::MetaPromotion**](MetaPromotion.md)> |  | [optional]
**creative_features** | Option<**std::collections::HashMap<String, Inner>**> | Meta Advantage+ creative enhancements. Map snake_case feature names to OPT_IN or OPT_OUT; Meta validates supported keys and unspecified features default to OPT_OUT. auto_promotion_tag is an enhancement; use the separate promotion field for an explicit offer. The deprecated standard_enhancements bundle is rejected by Meta. (enum: OPT_IN, OPT_OUT) | [optional]
**headline** | Option<**String**> | Meta and LinkedIn (TikTok has no headline slot) | [optional]
**body** | Option<**String**> |  | [optional]
**description** | Option<**String**> | Link description slot (Meta `link_data.description` / `video_data.link_description`, LinkedIn creative description). | [optional]
**call_to_action** | Option<**String**> |  | [optional]
**link_url** | Option<**String**> |  | [optional]
**image_url** | Option<**String**> |  | [optional]
**video_url** | Option<**String**> |  | [optional]
**video_id** | Option<**String**> | Meta only. Reuse an already-uploaded ad video (from POST /v1/ads/videos or GET /v1/ads/videos) instead of re-uploading via videoUrl. | [optional]
**existing_creative_id** | Option<**String**> | Meta only. Repoint the ad at an existing library creative (from GET /v1/ads/creatives); all other creative fields are ignored. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


