# StartSmsRegistrationRequestCampaign

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**usecase** | **String** |  | 
**sub_usecases** | Option<**Vec<SubUsecases>**> | The concrete kinds of messages a MIXED campaign sends (the carrier registry requires 2-5, and reviewers match them against the sample messages). Omitted: a default pair is applied for MIXED.  (enum: 2FA, ACCOUNT_NOTIFICATION, CUSTOMER_CARE, DELIVERY_NOTIFICATION, FRAUD_ALERT, HIGHER_EDUCATION, MARKETING, POLLING_VOTING, PUBLIC_SERVICE_ANNOUNCEMENT, SECURITY_ALERT) | [optional]
**description** | **String** |  | 
**message_flow** | **String** | How a recipient ends up receiving your messages (the opt-in flow). Include a link to the page or form where they opt in — carrier reviewers reject campaigns whose consent they can't verify. | 
**sample1** | **String** |  | 
**sample2** | **String** | Second example message; carriers require two distinct samples, so it must differ from sample1. | 
**help_message** | Option<**String**> |  | [optional]
**optin_keywords** | **String** |  | 
**optin_message** | Option<**String**> |  | [optional]
**optout_keywords** | **String** |  | 
**optout_message** | Option<**String**> |  | [optional]
**help_keywords** | **String** |  | 
**embedded_link** | Option<**bool**> | Whether messages carry links. Auto-derived from the samples when omitted, so the declaration matches what the reviewer reads. | [optional]
**embedded_phone** | Option<**bool**> | Whether messages carry phone numbers. Auto-derived from the samples when omitted. | [optional]
**number_pool** | Option<**bool**> |  | [optional]
**age_gated** | Option<**bool**> |  | [optional]
**direct_lending** | Option<**bool**> |  | [optional]
**privacy_policy_link** | Option<**String**> | Link to your privacy policy. Recommended: reviewers check that it says mobile information is not sold or shared with third parties for promotional purposes. A bare domain is normalized to https://. | [optional]
**terms_and_conditions_link** | Option<**String**> | Link to your terms & conditions. A bare domain is normalized to https://. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


