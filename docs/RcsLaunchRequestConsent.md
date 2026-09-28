# RcsLaunchRequestConsent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**opt_in_methods** | [**Vec<models::RcsLaunchRequestConsentOptInMethodsInner>**](RcsLaunchRequestConsentOptInMethodsInner.md) |  | 
**call_to_action** | **String** | The opt-in wording people agree to. | 
**call_to_action_url** | Option<**String**> | Required for WEBSITE opt-in. | [optional]
**call_to_action_media_url** | Option<**String**> | Screenshot of the opt-in. Required for WEBSITE and MOBILE_APP opt-in. | [optional]
**double_opt_in** | **bool** |  | 
**double_opt_in_message** | Option<**String**> | Required when doubleOptIn is true. | [optional]
**opt_in_message** | **String** |  | 
**help_response** | **String** |  | 
**opt_out_response** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


