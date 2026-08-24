# ConnectWhatsAppCredentials200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | Option<**String**> |  | [optional]
**registration_warning** | Option<**String**> | Present when the account was created but Meta rejected the Cloud API registration. The number cannot send messages until this is resolved. | [optional]
**webhook_notice** | Option<**String**> | Present when the WABA webhook subscription (with the Zernio override callback) succeeded. Explains the delivery cutover and warns against unsubscribing the app from the WABA afterward. | [optional]
**account** | Option<[**models::ConnectWhatsAppCredentials200ResponseAccount**](ConnectWhatsAppCredentials200ResponseAccount.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


