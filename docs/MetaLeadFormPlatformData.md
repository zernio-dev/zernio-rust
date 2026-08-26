# MetaLeadFormPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**questions** | [**Vec<models::CreateLeadFormRequestQuestionsInner>**](CreateLeadFormRequestQuestionsInner.md) |  | 
**privacy_policy_link_text** | Option<**String**> |  | [optional]
**follow_up_action_url** | Option<**String**> |  | [optional]
**locale** | Option<**String**> |  | [optional]
**thank_you_title** | Option<**String**> |  | [optional]
**thank_you_body** | Option<**String**> |  | [optional]
**thank_you_button_text** | Option<**String**> |  | [optional]
**thank_you_button_type** | Option<**String**> |  | [optional]
**thank_you_website_url** | Option<**String**> |  | [optional]
**thank_you_enable_messenger** | Option<**bool**> | Adds a 'Continue in Messenger' option to the thank-you page (Meta thank_you_page.enable_messenger), so the lead can carry on chatting with the Page. Set thankYouButtonType to MESSAGE_BUSINESS or P2B_MESSENGER to make the chat the primary button. | [optional][default to false]
**is_optimized_for_quality** | Option<**bool**> | Set true for a higher-intent form (adds a review step before submit). | [optional]
**is_phone_sms_verify_enabled** | Option<**bool**> | Requires the lead to verify their phone number over SMS before the form submits (Meta is_phone_sms_verify_enabled). Only meaningful on a form with a PHONE question. Meta can restrict this parameter to apps holding a capability: when it does, the create fails with a 422 naming platformSpecificData.isPhoneSmsVerifyEnabled, and the toggle then has to be set in Meta's form builder. | [optional][default to false]
**block_display_for_non_targeted_viewer** | Option<**bool**> |  | [optional]
**question_page_custom_headline** | Option<**String**> |  | [optional]
**context_card** | Option<[**models::MetaLeadFormPlatformDataContextCard**](MetaLeadFormPlatformDataContextCard.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


