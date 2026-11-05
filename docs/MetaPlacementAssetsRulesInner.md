# MetaPlacementAssetsRulesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**image_url** | Option<**String**> | Image mode. The image to deliver for this rule's placements. | [optional]
**video_url** | Option<**String**> | Video mode. The video to deliver for this rule's placements. Each rule needs this or `videoId`. | [optional]
**video_id** | Option<**String**> | Video mode. ID of a video already on the ad account, used for this rule instead of uploading `videoUrl`. Wins over `videoUrl`. A video still processing after 30 seconds returns 409. | [optional]
**thumbnail_url** | Option<**String**> | Video mode (optional). Poster image for this rule's video; auto-generated when omitted. | [optional]
**headline** | Option<**String**> | One headline pinned to this rule. Omit to inherit the top-level headline. | [optional]
**body** | Option<**String**> | One primary text pinned to this rule. Omit to inherit the top-level body. | [optional]
**description** | Option<**String**> | One link description pinned to this rule. Omit to inherit the top-level description. | [optional]
**placements** | [**models::MetaPlacementAssetsRulesInnerPlacements**](MetaPlacementAssetsRulesInnerPlacements.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


