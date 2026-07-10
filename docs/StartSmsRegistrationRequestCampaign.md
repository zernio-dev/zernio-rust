# StartSmsRegistrationRequestCampaign

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**usecase** | **String** |  | 
**sub_usecases** | Option<**Vec<SubUsecases>**> | The concrete kinds of messages a MIXED campaign sends (the carrier registry requires 2-5, and reviewers match them against the sample messages). Omitted: a default pair is applied for MIXED.  (enum: 2FA, ACCOUNT_NOTIFICATION, CUSTOMER_CARE, DELIVERY_NOTIFICATION, FRAUD_ALERT, HIGHER_EDUCATION, MARKETING, POLLING_VOTING, PUBLIC_SERVICE_ANNOUNCEMENT, SECURITY_ALERT) | [optional]
**description** | **String** |  | 
**message_flow** | **String** | How a recipient ends up receiving your messages (the opt-in flow). Include a link to the page or form where they opt in — carrier reviewers reject campaigns whose consent they can't verify. | 
**sample1** | **String** |  | 
**sample2** | **String** | Second example message; carriers require two distinct samples | 
**help_message** | **String** |  | 
**optin_keywords** | **String** |  | 
**optin_message** | **String** |  | 
**optout_keywords** | **String** |  | 
**optout_message** | **String** |  | 
**help_keywords** | **String** |  | 
**embedded_link** | Option<**bool**> |  | [optional]
**embedded_phone** | Option<**bool**> |  | [optional]
**number_pool** | Option<**bool**> |  | [optional]
**age_gated** | Option<**bool**> |  | [optional]
**direct_lending** | Option<**bool**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


