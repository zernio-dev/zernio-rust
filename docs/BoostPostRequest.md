# BoostPostRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**post_id** | Option<**String**> | Zernio post ID (provide this or platformPostId) | [optional]
**platform_post_id** | Option<**String**> | Platform post ID (alternative to postId) | [optional]
**account_id** | **String** | Social account ID | 
**ad_account_id** | **String** | Platform ad account ID | 
**name** | **String** |  | 
**goal** | **Goal** |  (enum: engagement, traffic, awareness, video_views) | 
**budget** | [**models::BoostPostRequestBudget**](BoostPostRequestBudget.md) |  | 
**currency** | Option<**String**> |  | [optional]
**schedule** | Option<[**models::BoostPostRequestSchedule**](BoostPostRequestSchedule.md)> |  | [optional]
**targeting** | Option<[**models::BoostPostRequestTargeting**](BoostPostRequestTargeting.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


