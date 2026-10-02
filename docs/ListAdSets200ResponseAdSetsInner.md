# ListAdSets200ResponseAdSetsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform_ad_set_id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**ad_set_name** | Option<**String**> |  | [optional]
**status** | Option<**String**> |  | [optional]
**platform_ad_set_status** | Option<**String**> | Raw platform ad set status. On TikTok the ad group's own switch `operation_status` (ENABLE / DISABLE), independent of its campaign. | [optional]
**platform_campaign_id** | Option<**String**> |  | [optional]
**platform_ad_account_id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**profile_id** | Option<**String**> |  | [optional]
**currency** | Option<**String**> |  | [optional]
**budget** | Option<[**models::ListAdSets200ResponseAdSetsInnerBudget**](ListAdSets200ResponseAdSetsInnerBudget.md)> |  | [optional]
**schedule** | Option<[**models::ListAdSets200ResponseAdSetsInnerSchedule**](ListAdSets200ResponseAdSetsInnerSchedule.md)> |  | [optional]
**targeting** | Option<[**models::ListAdSets200ResponseAdSetsInnerTargeting**](ListAdSets200ResponseAdSetsInnerTargeting.md)> |  | [optional]
**is_external** | Option<**bool**> |  | [optional]
**platform_created_at** | Option<**String**> |  | [optional]
**status_read_at** | Option<**String**> | Only with `live=true`. When `platformAdSetStatus` was read from the platform; null when this row was not read live. | [optional]
**optimization_goal** | Option<**String**> | TikTok only, only with `live=true` and only on rows read live. The ad group's `optimization_goal` exactly as TikTok's adgroup/get returns it now (for example ENGAGED_VIEW, ENGAGED_VIEW_FIFTEEN, CLICK, CONVERT). Absent on rows not read live and on other platforms. | [optional]
**billing_event** | Option<**String**> | TikTok only, only with `live=true` and only on rows read live. The ad group's `billing_event` exactly as TikTok's adgroup/get returns it now (for example CPV, CPC, OCPM). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


