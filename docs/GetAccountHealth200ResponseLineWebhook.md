# GetAccountHealth200ResponseLineWebhook

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**active** | Option<**bool**> | `false`: Webhooks are turned off in LINE Official Account Manager (LINE Developers Console: Use webhook), so LINE sends no messages to Zernio; turn it on in Settings > Response settings. `null`: LINE could not be read, not evidence either way. | [optional]
**destination** | Option<**Destination**> | Where the channel's webhook URL points.  - `zernio`: the URL Zernio set for this account. - `another_zernio_account`: another Zernio account connected to the same channel, which receives its events instead. - `other`: another integration's URL (reconnect the account to point it back). - `missing`: no URL is set. - `null`: LINE could not be read.  (enum: zernio, another_zernio_account, other, missing, ) | [optional]
**checked_at** | Option<**String**> | When this live read ran (always the current request; never cached) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


