# MetaPlacementAssets

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**default_image_url** | Option<**String**> | Image mode. Catch-all image for any placement no rule matches. Required in image mode (Meta mandates a default rule). | [optional]
**default_video_url** | Option<**String**> | Video mode. Catch-all video for any placement no rule matches. Video mode requires this or `defaultVideoId`. | [optional]
**default_video_id** | Option<**String**> | Video mode. ID of a video already on the ad account, used as the catch-all instead of uploading `defaultVideoUrl`. Wins over `defaultVideoUrl`. A video still processing after 30 seconds returns 409. | [optional]
**default_thumbnail_url** | Option<**String**> | Video mode (optional). Poster image for the default video; Meta auto-generates one when omitted. | [optional]
**rules** | [**Vec<models::MetaPlacementAssetsRulesInner>**](MetaPlacementAssetsRulesInner.md) | One entry per placement group you want to pin a specific asset to. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


