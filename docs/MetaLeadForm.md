# MetaLeadForm

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**status** | Option<**String**> | One of ACTIVE, ARCHIVED, DELETED or DRAFT. | [optional]
**locale** | Option<**String**> |  | [optional]
**created_time** | Option<**String**> |  | [optional]
**page_id** | Option<**String**> | Owning Facebook Page. A form on any other Page is a 404, whether read or archived. | [optional]
**leads_count** | Option<**i32**> |  | [optional]
**organic_leads_count** | Option<**i32**> |  | [optional]
**expired_leads_count** | Option<**i32**> | Leads Meta has aged out of the retention window. | [optional]
**privacy_policy_url** | Option<**String**> |  | [optional]
**follow_up_action_url** | Option<**String**> |  | [optional]
**follow_up_action_text** | Option<**String**> |  | [optional]
**question_page_custom_headline** | Option<**String**> |  | [optional]
**is_optimized_for_quality** | Option<**bool**> |  | [optional]
**block_display_for_non_targeted_viewer** | Option<**bool**> |  | [optional]
**allow_organic_lead** | Option<**bool**> | Whether the form can also be submitted from an organic Page post. | [optional]
**tracking_parameters** | Option<[**Vec<models::BoostPostRequestTrackingUrlTagsInner>**](BoostPostRequestTrackingUrlTagsInner.md)> | Custom key/value pairs attached to every lead of this form. | [optional]
**legal_content** | Option<[**models::MetaLeadFormLegalContent**](MetaLeadFormLegalContent.md)> |  | [optional]
**context_card** | Option<[**models::MetaLeadFormContextCard**](MetaLeadFormContextCard.md)> |  | [optional]
**thank_you_page** | Option<[**models::MetaLeadFormThankYouPage**](MetaLeadFormThankYouPage.md)> |  | [optional]
**questions** | Option<[**Vec<models::MetaLeadFormQuestionsInner>**](MetaLeadFormQuestionsInner.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


