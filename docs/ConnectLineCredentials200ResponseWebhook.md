# ConnectLineCredentials200ResponseWebhook

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**url** | Option<**String**> | The webhook URL Zernio set on the channel. | [optional]
**configured** | Option<**bool**> | Whether LINE accepted the webhook URL. When false, paste `url` into the LINE Developers Console > Messaging API > Webhook URL yourself. | [optional]
**test_succeeded** | Option<**bool**> | Whether LINE's webhook test call reached Zernio. It does not show whether Webhooks is turned on; read `active` for that. | [optional]
**active** | Option<**bool**> | Whether Webhooks (LINE Developers Console: Use webhook) is turned on for the channel, read after Zernio set its URL.  `false` means LINE sends no events until the account owner turns it on in LINE Official Account Manager > Settings > Response settings. `null` when LINE did not answer the read, and always when `configured` is `false`.  | [optional]
**detail** | Option<**String**> | What LINE answered when the setup or the test did not succeed. | [optional]
**previous_url** | Option<**String**> | Present when the channel pointed at another webhook URL before this connect. LINE allows one webhook URL per channel, so that URL stopped receiving events once Zernio set its own; `nextSteps` says so too. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


