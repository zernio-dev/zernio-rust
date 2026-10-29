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
**thank_you_button_type** | Option<**String**> | Meta thank_you_page.button_type. Defaults to VIEW_WEBSITE. Case-insensitive, sent to Meta in uppercase. CALL_BUSINESS requires businessPhoneNumber and countryCode (a 400 otherwise). Meta rejects MESSAGE_BUSINESS on thank-you pages with (#100) This button type is not yet supported for Thank You Page. | [optional]
**business_phone_number** | Option<**String**> | International E.164 number the CALL_BUSINESS thank-you button dials (Meta thank_you_page.business_phone_number).  - Must start with + and the country calling code matching countryCode. Spaces, dashes, dots and parentheses are stripped; a local number such as 2025550123 is a 400. - Required when thankYouButtonType is CALL_BUSINESS; a 400 with any other button type. - Accepted only inside platformSpecificData; a top-level businessPhoneNumber is a 400. | [optional]
**country_code** | Option<**String**> | ISO 3166-1 alpha-2 country of businessPhoneNumber (Meta thank_you_page.country_code), sent in uppercase. Required when thankYouButtonType is CALL_BUSINESS and a 400 with any other button type. Accepted only inside platformSpecificData: a top-level countryCode is a 400. | [optional]
**thank_you_website_url** | Option<**String**> |  | [optional]
**thank_you_enable_messenger** | Option<**bool**> | Sent as Meta thank_you_page.enable_messenger (boolean). Accepted only inside platformSpecificData: a top-level thankYouEnableMessenger is a 400. | [optional][default to false]
**is_optimized_for_quality** | Option<**bool**> | Set true for a higher-intent form (adds a review step before submit). | [optional]
**is_phone_sms_verify_enabled** | Option<**bool**> | Requires the lead to verify their phone number over SMS before the form submits (Meta is_phone_sms_verify_enabled). Only meaningful on a form with a PHONE question.  Meta can restrict this parameter to apps holding a capability. When it does, the create fails with a 422 naming platformSpecificData.isPhoneSmsVerifyEnabled, and the toggle must then be set in Meta's form builder. | [optional][default to false]
**block_display_for_non_targeted_viewer** | Option<**bool**> |  | [optional]
**question_page_custom_headline** | Option<**String**> |  | [optional]
**context_card** | Option<[**models::MetaLeadFormPlatformDataContextCard**](MetaLeadFormPlatformDataContextCard.md)> |  | [optional]
**custom_disclaimer** | Option<[**models::MetaLeadFormPlatformDataCustomDisclaimer**](MetaLeadFormPlatformDataCustomDisclaimer.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


