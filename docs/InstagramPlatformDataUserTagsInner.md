# InstagramPlatformDataUserTagsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**username** | **String** | Instagram username (@ symbol is optional and will be removed automatically) | 
**x** | Option<**f64**> | X coordinate position from left edge (0.0 = left, 0.5 = center, 1.0 = right). Required for photos, ignored for Reels/videos, optional for stories. | [optional]
**y** | Option<**f64**> | Y coordinate position from top edge (0.0 = top, 0.5 = center, 1.0 = bottom). Required for photos, ignored for Reels/videos, optional for stories. | [optional]
**media_index** | Option<**i32**> | Zero-based index of the carousel item to tag. Defaults to 0. Tags on out-of-range indices are ignored. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


