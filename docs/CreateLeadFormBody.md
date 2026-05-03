# CreateLeadFormBody

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Facebook social account ID (Late SocialAccount _id). | 
**name** | **String** |  | 
**questions** | [**Vec<models::LeadGenFormQuestion>**](LeadGenFormQuestion.md) |  | 
**privacy_policy_url** | **String** | Required by Meta. Must be reachable from Meta's crawler. | 
**privacy_policy_link_text** | Option<**String**> |  | [optional]
**follow_up_action_url** | Option<**String**> |  | [optional]
**locale** | Option<**String**> |  | [optional]
**thank_you_title** | Option<**String**> |  | [optional]
**thank_you_body** | Option<**String**> |  | [optional]
**thank_you_button_text** | Option<**String**> |  | [optional]
**thank_you_button_type** | Option<**String**> | Meta enum (e.g. VIEW_WEBSITE, CALL_BUSINESS, DOWNLOAD) | [optional]
**thank_you_website_url** | Option<**String**> |  | [optional]
**is_optimized_for_quality** | Option<**bool**> |  | [optional]
**context_card** | Option<[**models::CreateLeadFormBodyContextCard**](CreateLeadFormBodyContextCard.md)> |  | [optional]
**legal_content** | Option<[**models::CreateLeadFormBodyLegalContent**](CreateLeadFormBodyLegalContent.md)> |  | [optional]
**tracking_parameters** | Option<**std::collections::HashMap<String, String>**> | Up to 20 key/value pairs surfaced on every lead for attribution. | [optional]
**question_page_custom_headline** | Option<**String**> |  | [optional]
**allow_organic_lead** | Option<**bool**> |  | [optional]
**block_display_for_non_targeted_viewer** | Option<**bool**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


