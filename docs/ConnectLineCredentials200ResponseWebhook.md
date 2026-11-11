# ConnectLineCredentials200ResponseWebhook

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | Option<**String**> | The webhook URL Zernio set on the channel. | [optional]
**configured** | Option<**bool**> | Whether LINE accepted the webhook URL. When false, paste `url` into the LINE Developers Console > Messaging API > Webhook URL yourself. | [optional]
**test_succeeded** | Option<**bool**> | Whether LINE's webhook test call reached Zernio. | [optional]
**detail** | Option<**String**> | What LINE answered when the setup or the test did not succeed. | [optional]
**previous_url** | Option<**String**> | Present when the channel pointed at another webhook URL before this connect. LINE allows one webhook URL per channel, so that URL stopped receiving events once Zernio set its own; `nextSteps` says so too. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


