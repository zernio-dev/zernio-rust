# GenerateAdPreviewsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id used to resolve the Meta token. | 
**ad_account_id** | **String** | Meta ad account id (act_<n>). | 
**formats** | Option<**Vec<String>**> | Meta ad_format values, one preview per format. Defaults to [DESKTOP_FEED_STANDARD]. | [optional]
**existing_creative_id** | Option<**String**> | Preview an existing ad-account creative by id. Mutually exclusive with creativeSpec. | [optional]
**creative_spec** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Raw Meta creative spec forwarded verbatim to /generatepreviews. Mutually exclusive with existingCreativeId. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


