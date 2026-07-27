# CreateLeadFormRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**name** | **String** |  | 
**questions** | Option<[**Vec<models::CreateLeadFormRequestQuestionsInner>**](CreateLeadFormRequestQuestionsInner.md)> | Deprecated (Meta legacy shape): use platformSpecificData.questions. | [optional]
**privacy_policy_url** | **String** |  | 
**privacy_policy_link_text** | Option<**String**> | Deprecated: use platformSpecificData.privacyPolicyLinkText. | [optional]
**follow_up_action_url** | Option<**String**> | Deprecated: use platformSpecificData.followUpActionUrl. | [optional]
**locale** | Option<**String**> | Deprecated: use platformSpecificData.locale. | [optional]
**thank_you_title** | Option<**String**> | Deprecated: use platformSpecificData.thankYouTitle. | [optional]
**thank_you_body** | Option<**String**> | Deprecated: use platformSpecificData.thankYouBody. | [optional]
**thank_you_button_text** | Option<**String**> | Deprecated: use platformSpecificData.thankYouButtonText. | [optional]
**thank_you_button_type** | Option<**String**> | Deprecated: use platformSpecificData.thankYouButtonType. | [optional]
**thank_you_website_url** | Option<**String**> | Deprecated: use platformSpecificData.thankYouWebsiteUrl. | [optional]
**is_optimized_for_quality** | Option<**bool**> | Deprecated: use platformSpecificData.isOptimizedForQuality. | [optional]
**platform_specific_data** | Option<[**models::CreateLeadFormRequestPlatformSpecificData**](CreateLeadFormRequestPlatformSpecificData.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


