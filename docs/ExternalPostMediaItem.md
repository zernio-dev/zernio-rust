# ExternalPostMediaItem

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** |  (enum: image, video) | 
**url** | Option<**String**> | 'Direct URL to the media file. Null when the platform withholds it: check mediaStatus before downloading. Instagram omits the video file for Reels it flags as containing copyrighted material (its docs name audio as the usual cause), so type stays \"video\" while the file is permanently unreachable. For LinkedIn videos where the platform returns no file, url falls back to the cover image and the item carries mediaStatus: unavailable.' | 
**thumbnail** | Option<**String**> | Cover image. Still present when url is null. | [optional]
**media_status** | Option<**MediaStatus**> | unavailable means the media file could not be retrieved (url is null or, for LinkedIn videos, a cover image standing in for the file). available or absent means the file is available at url (older synced items omit the field). (enum: available, unavailable) | [optional]
**unavailable_reason** | Option<**UnavailableReason**> | Why the file is missing. platform_withheld means the platform declined to return it and retrying will not help. (enum: platform_withheld) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


