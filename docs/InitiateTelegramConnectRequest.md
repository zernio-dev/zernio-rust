# InitiateTelegramConnectRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**chat_id** | **String** | The Telegram chat ID. Numeric ID (e.g. \"-1001234567890\") or username with @ prefix (e.g. \"@mychannel\"). | 
**profile_id** | **String** | The profile ID to connect the account to | 
**purpose** | Option<**Purpose**> | Connect the account for notifications only. Slack and Telegram only: `GET /v1/connect/{platform}` returns 400 for any other platform, and other platforms' own connect endpoints ignore it.  The account is free, receives Zernio notifications, and cannot publish. To publish with it, connect it again without `purpose`. Refused with 400 when the channel or chat is already connected for publishing: connect a separate one for notifications. (enum: notifications) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


