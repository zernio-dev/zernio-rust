# CreateStandaloneAdRequestPlacementAssets

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**default_image_url** | Option<**String**> | Image mode. Catch-all image for any placement no rule matches. Required in image mode (Meta mandates a default rule). | [optional]
**default_video_url** | Option<**String**> | Video mode. Catch-all video for any placement no rule matches. Required in video mode. | [optional]
**default_thumbnail_url** | Option<**String**> | Video mode (optional). Poster image for the default video; Meta auto-generates one when omitted. | [optional]
**rules** | [**Vec<models::CreateStandaloneAdRequestPlacementAssetsRulesInner>**](CreateStandaloneAdRequestPlacementAssetsRulesInner.md) | One entry per placement group you want to pin a specific asset to. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


