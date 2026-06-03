# UpdateAdTrackingTagsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url_tags** | Option<[**Vec<models::UpdateAdTrackingTagsRequestUrlTagsInner>**](UpdateAdTrackingTagsRequestUrlTagsInner.md)> | Meta only. Click-URL params appended to a freshly-rebuilt creative. | [optional]
**creative** | Option<[**models::UpdateAdTrackingTagsRequestCreative**](UpdateAdTrackingTagsRequestCreative.md)> |  | [optional]
**tracking_url_template** | Option<**String**> | Google only. Full tracking template (must contain {lpurl}). | [optional]
**final_url_suffix** | Option<**String**> | Google only. Parse-only key=value params. | [optional]
**dynamic_value_parameters** | Option<**std::collections::HashMap<String, String>**> | LinkedIn only. key -> dynamic value enum (CAMPAIGN_ID, CAMPAIGN_NAME, CREATIVE_ID, ...). | [optional]
**custom_value_parameters** | Option<**std::collections::HashMap<String, String>**> | LinkedIn only. key -> static value. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


