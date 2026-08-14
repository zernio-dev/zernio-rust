# AnalyticsSinglePostResponseMediaItemsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | Option<**Type**> |  (enum: image, video) | [optional]
**url** | Option<**String**> | 'Direct URL to the media file. Null when the platform withholds it: check mediaStatus before downloading. Instagram omits the video file for Reels it flags as containing copyrighted material (its docs name audio as the usual cause), so type stays \"video\" while the file is permanently unreachable.' | [optional]
**thumbnail** | Option<**String**> | Thumbnail URL (same as url for images). Still present when url is null. | [optional]
**alt_text** | Option<**String**> | Accessibility alt text set on the media, when present. | [optional]
**media_status** | Option<**MediaStatus**> | Present only when the media file could not be retrieved. Absent means the file is available at url. (enum: unavailable) | [optional]
**unavailable_reason** | Option<**UnavailableReason**> | Why the file is missing. platform_withheld means the platform declined to return it and retrying will not help. (enum: platform_withheld) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


