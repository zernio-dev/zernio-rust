# InstagramAudioAsset

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**audio_id** | Option<**String**> | Audio asset ID. Pass it as platformSpecificData.audioConfiguration.audioId when creating a Reel. | [optional]
**title** | Option<**String**> | Track or sound title. | [optional]
**audio_type** | Option<**AudioType**> | Catalog type of the asset. (enum: music, original_sound, ) | [optional]
**duration_in_ms** | Option<**i32**> | Asset duration in milliseconds. | [optional]
**display_artist** | Option<**String**> | Artist name (licensed music only). | [optional]
**cover_artwork_thumbnail_url** | Option<**String**> | Cover artwork thumbnail (licensed music only). | [optional]
**download_url** | Option<**String**> | Temporary preview URL. Meta expires it after roughly 1.5 days; re-fetch the asset to refresh it. | [optional]
**ig_username** | Option<**String**> | Creator username (original sounds only). | [optional]
**profile_picture_url** | Option<**String**> | Creator profile picture (original sounds only). | [optional]
**is_ads_eligible** | Option<**bool**> | Whether the asset is eligible for ads use. | [optional]
**on_platform_audio_preview_link** | Option<**String**> | Instagram web link to preview the audio. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


