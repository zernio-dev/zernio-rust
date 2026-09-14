# TikTokPlatformDataMusicSoundInfo

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**music_sound_id** | **String** | The id field of a track from GET /v1/accounts/{accountId}/tiktok/commercial-music (a song clip id). TikTok fails the publish with a generic 51065 when given the commercial music id instead. | 
**music_sound_volume** | Option<**i32**> | Track volume. TikTok defaults an omitted volume to 0, which publishes the track silently, so we default to the app's 50. Video posts only. | [optional][default to 50]
**music_sound_start** | Option<**i32**> | Start point of the track in milliseconds (default 0). Video posts only. | [optional]
**music_sound_end** | Option<**i32**> | End point of the track in milliseconds (default: the video length). Must be greater than musicSoundStart. Video posts only. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


