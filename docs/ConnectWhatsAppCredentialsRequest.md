# ConnectWhatsAppCredentialsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** | Your Zernio profile ID | 
**access_token** | **String** | Permanent System User access token from Meta Business Suite | 
**waba_id** | **String** | WhatsApp Business Account ID from Meta | 
**phone_number_id** | **String** | Phone Number ID from Meta WhatsApp Manager | 
**pin** | Option<**String**> | The 6-digit two-step verification PIN set on the number. Required if you enabled two-step verification for it, otherwise Meta rejects the Cloud API registration with error 133005 and the number cannot send messages. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


