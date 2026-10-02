# ConnectSlackChannelRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**channel_id** | Option<**String**> | Slack channel id, C... or G.... Send this or channelIds, not both. | [optional]
**channel_ids** | Option<**Vec<String>**> | Several channels of the workspace to connect, each as its own account. With two or more distinct ids the response lists `accounts` and `failed` instead of `account`, and the request is refused with 400 on a reconnect. A single id behaves exactly like channelId. | [optional]
**redirect_url** | Option<**String**> | channelIds only: a URL to return in `redirect_url`, with `connected`, `profileId`, `accountId` and `accountIds` appended. | [optional]
**pending_data_token** | Option<**String**> | Nonce from the OAuth redirect. Required unless accountId is sent. | [optional]
**account_id** | Option<**String**> | Existing Slack account whose workspace token is reused. Required unless pendingDataToken is sent. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


