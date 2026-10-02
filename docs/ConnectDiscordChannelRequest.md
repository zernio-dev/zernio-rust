# ConnectDiscordChannelRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**guild_id** | **String** | Discord server (guild) the channel belongs to | 
**channel_id** | Option<**String**> | Text, announcement or forum channel to publish to. Send this or channelIds, not both. | [optional]
**channel_ids** | Option<**Vec<String>**> | Several channels of the server to connect, each as its own account. With two or more distinct ids the response lists `accounts` and `failed` instead of `account`. A single id behaves exactly like channelId. | [optional]
**profile_id** | **String** | Profile to connect the channel to | 
**redirect_url** | Option<**String**> | channelIds only: a URL to return in `redirect_url`, with `connected`, `profileId`, `accountId` and `accountIds` appended. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


