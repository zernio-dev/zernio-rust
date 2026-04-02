# Ad

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: facebook, instagram, tiktok, linkedin, pinterest, google, twitter) | [optional]
**status** | Option<**Status**> |  (enum: active, paused, pending_review, rejected, completed, cancelled, error) | [optional]
**ad_type** | Option<**AdType**> |  (enum: boost, standalone) | [optional]
**goal** | Option<**Goal**> |  (enum: engagement, traffic, awareness, video_views) | [optional]
**is_external** | Option<**bool**> | True for ads synced from platform ad managers | [optional]
**budget** | Option<[**models::AdBudget**](AdBudget.md)> |  | [optional]
**metrics** | Option<[**models::AdMetrics**](AdMetrics.md)> |  | [optional]
**platform_ad_id** | Option<**String**> |  | [optional]
**platform_ad_account_id** | Option<**String**> |  | [optional]
**platform_campaign_id** | Option<**String**> |  | [optional]
**platform_ad_set_id** | Option<**String**> |  | [optional]
**campaign_name** | Option<**String**> |  | [optional]
**ad_set_name** | Option<**String**> |  | [optional]
**creative** | Option<[**models::AdCreative**](AdCreative.md)> |  | [optional]
**targeting** | Option<**serde_json::Value**> |  | [optional]
**schedule** | Option<[**models::AdSchedule**](AdSchedule.md)> |  | [optional]
**rejection_reason** | Option<**String**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


