# ConnectSlackChannelRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**channel_id** | **String** | Slack channel id, C... or G... | 
**pending_data_token** | Option<**String**> | Nonce from the OAuth redirect. Required unless accountId is sent. | [optional]
**account_id** | Option<**String**> | Existing Slack account whose workspace token is reused. Required unless pendingDataToken is sent. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


