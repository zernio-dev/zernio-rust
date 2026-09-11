# GooglePmaxAssetGroupUpdate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**final_url** | Option<**String**> | Replaces the asset group's final URL. | [optional]
**headlines** | Option<**HashSet<String>**> | Replaces every HEADLINE asset on the group. | [optional]
**long_headline** | Option<**String**> | Replaces the LONG_HEADLINE asset. | [optional]
**descriptions** | Option<**HashSet<String>**> | Replaces every DESCRIPTION asset. At least one must be 60 characters or fewer. | [optional]
**business_name** | Option<**String**> | Replaces the BUSINESS_NAME asset. | [optional]
**images** | Option<[**models::GooglePmaxAssetGroupUpdateImages**](GooglePmaxAssetGroupUpdateImages.md)> |  | [optional]
**youtube_video_ids** | Option<**Vec<String>**> | Replaces YOUTUBE_VIDEO assets with existing YouTube video ids. Video uploads and arbitrary video URLs are not supported. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


