# SendDiscordDirectMessageRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | SocialAccount _id of the connected Discord account the bot speaks as. Caller must own the account (directly or via team membership). | 
**user_id** | **String** | Discord snowflake ID of the recipient (15-21 digits). | 
**content** | Option<**String**> | Message text, up to 2,000 characters. | [optional]
**embeds** | Option<**Vec<serde_json::Value>**> | Up to 10 Discord embeds. Same shape as channel-post embeds (title, description, color, fields, etc.). See DiscordPlatformData.embeds for the embed object schema. | [optional]
**attachments** | Option<[**Vec<models::SendDiscordDirectMessageRequestAttachmentsInner>**](SendDiscordDirectMessageRequestAttachmentsInner.md)> | Up to 10 media attachments. Each is `{ type: image|video|gif|document, url, filename?, mimeType?, size? }`. | [optional]
**tts** | Option<**bool**> | Send as text-to-speech message. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


