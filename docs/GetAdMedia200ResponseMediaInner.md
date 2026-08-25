# GetAdMedia200ResponseMediaInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | Option<**Type**> |  (enum: image, video) | [optional]
**url** | Option<**String**> | Direct file URL (signed; short-lived — see description). | [optional]
**thumbnail_url** | Option<**String**> | Video poster URL (videos only). | [optional]
**video_id** | Option<**String**> | Meta video id (videos only), reusable as video.id on the create endpoints. | [optional]
**length** | Option<**f64**> | Video length in seconds (videos only). | [optional]
**index** | Option<**i32**> | 0-based position for carousel children or asset_feed_spec entries. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


