# ConnectLineCredentials200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | Option<**String**> |  | [optional]
**account** | Option<[**models::ConnectedMessagingAccount**](ConnectedMessagingAccount.md)> |  | [optional]
**webhook** | Option<[**models::ConnectLineCredentials200ResponseWebhook**](ConnectLineCredentials200ResponseWebhook.md)> |  | [optional]
**next_steps** | Option<**Vec<String>**> | Settings the account owner still has to change in LINE Official Account Manager, led by a warning when `webhook.previousUrl` is set. | [optional]
**redirect_url** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


