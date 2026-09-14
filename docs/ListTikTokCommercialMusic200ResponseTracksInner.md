# ListTikTokCommercialMusic200ResponseTracksInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | The id to send as musicSoundId (the full track's song clip id). TikTok rejects the commercial music id itself at publish time. | [optional]
**commercial_music_id** | Option<**String**> | TikTok's commercial_music_id, for reference only | [optional]
**name** | Option<**String**> |  | [optional]
**artist** | Option<**String**> |  | [optional]
**duration_sec** | Option<**i32**> |  | [optional]
**genres** | Option<**Vec<String>**> |  | [optional]
**preview_url** | Option<**String**> | Preview audio of the full track | [optional]
**thumbnail_url** | Option<**String**> |  | [optional]
**rank** | Option<**i32**> | Position in the trending chart, 1 first | [optional]
**clip** | Option<[**models::ListTikTokCommercialMusic200ResponseTracksInnerClip**](ListTikTokCommercialMusic200ResponseTracksInnerClip.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


