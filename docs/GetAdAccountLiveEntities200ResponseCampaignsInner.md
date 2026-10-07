# GetAdAccountLiveEntities200ResponseCampaignsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform_campaign_id** | Option<**String**> |  | [optional]
**campaign_name** | Option<**String**> |  | [optional]
**platform_campaign_status** | Option<**String**> | Meta `effective_status` (ACTIVE, PAUSED, WITH_ISSUES...) or TikTok `secondary_status` (CAMPAIGN_STATUS_ENABLE...). | [optional]
**configured_status** | Option<**String**> | The campaign's own switch: Meta `status` (ACTIVE, PAUSED, DELETED, ARCHIVED), or TikTok `operation_status` as ACTIVE (ENABLE) / PAUSED (DISABLE). | [optional]
**status** | Option<**String**> | Zernio's normalized status (active, paused, ...), derived from `platformCampaignStatus`. | [optional]
**budget** | Option<[**models::GetAdAccountLiveEntities200ResponseCampaignsInnerBudget**](GetAdAccountLiveEntities200ResponseCampaignsInnerBudget.md)> |  | [optional]
**daily_budget** | Option<**f64**> | Daily budget in whole units of `currency` (Meta `daily_budget`; TikTok `budget` under a daily budget mode). | [optional]
**lifetime_budget** | Option<**f64**> | Lifetime budget in whole units of `currency` (Meta `lifetime_budget`; TikTok `budget` under BUDGET_MODE_TOTAL). | [optional]
**budget_mode** | Option<**String**> | TikTok only: `budget_mode` as TikTok reports it (BUDGET_MODE_DAY, BUDGET_MODE_DYNAMIC_DAILY_BUDGET, BUDGET_MODE_TOTAL, BUDGET_MODE_INFINITE). | [optional]
**budget_remaining** | Option<**f64**> | Meta `budget_remaining` in whole units of `currency`. Null when the campaign has no budget of its own, and always on TikTok. | [optional]
**spend_cap** | Option<**f64**> | Campaign spending limit (Meta `spend_cap`) in whole units of `currency`. Null when none is set, and always on TikTok. | [optional]
**bid_strategy** | Option<**String**> | Meta `bid_strategy`, set on campaigns with a campaign budget. Null on TikTok. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


