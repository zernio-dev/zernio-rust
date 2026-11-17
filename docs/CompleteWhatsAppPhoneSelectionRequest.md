# CompleteWhatsAppPhoneSelectionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** | The Zernio profile ID | 
**phone_number_id** | **String** | The selected phone number ID (from listWhatsAppPhoneNumbers) | 
**waba_id** | **String** | The WABA ID containing the selected phone | 
**temp_token** | Option<**String**> | The temporary access token from the headless redirect. Required unless sent in the X-Temp-Token header. | [optional]
**connect_flow** | Option<**String**> | Set by the Zernio-hosted picker, whose user token stays in an httpOnly cookie. Integrators send tempToken instead. | [optional]
**user_profile** | Option<**serde_json::Value**> | Optional user profile data (passthrough) | [optional]
**redirect_url** | Option<**String**> | Optional URL to receive the post-connection redirect target | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


