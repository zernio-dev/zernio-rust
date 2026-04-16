# DiscordPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel_id** | **String** | Target channel snowflake ID. Determines which channel in the connected server receives the message. | 
**embeds** | Option<[**Vec<models::DiscordPlatformDataEmbedsInner>**](DiscordPlatformDataEmbedsInner.md)> | Up to 10 Discord embed objects (combined max 6,000 characters across all embeds). Sent alongside or instead of plain-text content. | [optional]
**poll** | Option<[**models::DiscordPlatformDataPoll**](DiscordPlatformDataPoll.md)> |  | [optional]
**crosspost** | Option<**bool**> | Auto-crosspost to every server following this announcement channel (type 5). No-op for regular text channels. | [optional]
**forum_thread_name** | Option<**String**> | Thread title for forum channel posts (type 15). Required when posting to a forum channel. | [optional]
**forum_applied_tags** | Option<**Vec<String>**> | Tag snowflake IDs to apply to forum posts. Max 5 tags. | [optional]
**thread_from_message** | Option<[**models::DiscordPlatformDataThreadFromMessage**](DiscordPlatformDataThreadFromMessage.md)> |  | [optional]
**tts** | Option<**bool**> | Send as text-to-speech message. Discord reads the message aloud in the channel. | [optional]
**webhook_username** | Option<**String**> | Override the webhook display name for this post only (1-80 chars). Falls back to the account-level default set via PATCH /v1/connect/discord. | [optional]
**webhook_avatar_url** | Option<**String**> | Override the webhook avatar URL for this post only. Falls back to the account-level default. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


