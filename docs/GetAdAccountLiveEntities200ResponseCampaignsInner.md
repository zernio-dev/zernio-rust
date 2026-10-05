# GetAdAccountLiveEntities200ResponseCampaignsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform_campaign_id** | Option<**String**> |  | [optional]
**campaign_name** | Option<**String**> |  | [optional]
**platform_campaign_status** | Option<**String**> | Meta `effective_status`, for example ACTIVE, PAUSED, WITH_ISSUES. | [optional]
**configured_status** | Option<**String**> | Meta `status`: the campaign's own switch (ACTIVE, PAUSED, DELETED, ARCHIVED). | [optional]
**status** | Option<**String**> | Zernio's normalized status (active, paused, ...), derived from `platformCampaignStatus`. | [optional]
**budget** | Option<[**models::GetAdAccountLiveEntities200ResponseCampaignsInnerBudget**](GetAdAccountLiveEntities200ResponseCampaignsInnerBudget.md)> |  | [optional]
**daily_budget** | Option<**f64**> | Meta `daily_budget` in whole units of `currency`. | [optional]
**lifetime_budget** | Option<**f64**> | Meta `lifetime_budget` in whole units of `currency`. | [optional]
**budget_remaining** | Option<**f64**> | Meta `budget_remaining` in whole units of `currency`. Null when the campaign has no budget of its own. | [optional]
**spend_cap** | Option<**f64**> | Campaign spending limit (Meta `spend_cap`) in whole units of `currency`. Null when none is set. | [optional]
**bid_strategy** | Option<**String**> | Meta `bid_strategy`, set on campaigns with a campaign budget. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


