# DiscordScheduledEvent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Event snowflake ID | [optional]
**guild_id** | Option<**String**> |  | [optional]
**channel_id** | Option<**String**> | Voice/stage channel ID; null for external events. | [optional]
**creator_id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**description** | Option<**String**> |  | [optional]
**scheduled_start_time** | Option<**String**> |  | [optional]
**scheduled_end_time** | Option<**String**> | Required for external events; optional for voice/stage. | [optional]
**privacy_level** | Option<**PrivacyLevel**> | Always 2 (GUILD_ONLY) — Discord deprecated PUBLIC events. (enum: 2) | [optional]
**status** | Option<**Status**> | 1=SCHEDULED, 2=ACTIVE, 3=COMPLETED, 4=CANCELED (enum: 1, 2, 3, 4) | [optional]
**entity_type** | Option<**EntityType**> | 1=STAGE_INSTANCE, 2=VOICE, 3=EXTERNAL (enum: 1, 2, 3) | [optional]
**entity_id** | Option<**String**> |  | [optional]
**entity_metadata** | Option<[**models::DiscordScheduledEventEntityMetadata**](DiscordScheduledEventEntityMetadata.md)> |  | [optional]
**user_count** | Option<**i32**> | Number of members who RSVP'd. Only present when withUserCount=true on list. | [optional]
**image** | Option<**String**> | Cover image hash; build URL via cdn.discordapp.com. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


