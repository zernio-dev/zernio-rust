# ConnectLineCredentials200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | Option<**String**> |  | [optional]
**account** | Option<[**models::ConnectedMessagingAccount**](ConnectedMessagingAccount.md)> |  | [optional]
**webhook** | Option<[**models::ConnectLineCredentials200ResponseWebhook**](ConnectLineCredentials200ResponseWebhook.md)> |  | [optional]
**next_steps** | Option<**Vec<String>**> | Settings the account owner still has to change in LINE Official Account Manager. Led by the turn-on-Webhooks step when `webhook.active` is `false`, then by a warning when `webhook.previousUrl` is set. The turn-on-Webhooks step is left out when `webhook.active` is `true`. | [optional]
**redirect_url** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


