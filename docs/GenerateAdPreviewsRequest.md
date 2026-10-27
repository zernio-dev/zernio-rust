# GenerateAdPreviewsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id used to resolve the Meta token. | 
**ad_account_id** | **String** | Platform ad account id (Meta act_<n>, Google customer id, LinkedIn account id, ...). | 
**formats** | Option<**Vec<String>**> | Meta ad_format values, one preview per format. Defaults to [DESKTOP_FEED_STANDARD]. | [optional]
**existing_creative_id** | Option<**String**> | Preview an existing ad-account creative by id. Mutually exclusive with creativeSpec. | [optional]
**creative_spec** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Raw Meta creative spec forwarded to /generatepreviews. Mutually exclusive with existingCreativeId. An `object_story_spec` without `page_id` or `instagram_user_id`, and a `source_instagram_media_id` spec without `instagram_user_id`, get the connection's Facebook Page and Instagram account, as a create would. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


