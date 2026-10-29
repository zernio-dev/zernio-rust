# MetaAdsPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> |  | [optional]
**bid_amount** | Option<**f64**> | Whole currency units (USD: 5 = $5.00). Required when bidStrategy is LOWEST_COST_WITH_BID_CAP or COST_CAP.  May also be sent alone, WITHOUT bidStrategy, to set the cap on an ad set joining a COST_CAP / LOWEST_COST_WITH_BID_CAP campaign (the strategy is inherited from the campaign):  - POST /v1/ads/create: that shape requires existingCampaignId and is a 400 otherwise. - POST /v1/ads/boost: it is promoted to LOWEST_COST_WITH_BID_CAP. | [optional]
**roas_average_floor** | Option<**f64**> | Decimal ROAS multiplier (2.0 = 2.0x). Required when bidStrategy is LOWEST_COST_WITH_MIN_ROAS; sending it without bidStrategy is a 400. | [optional]
**daily_min_spend_target** | Option<**f64**> | Meta daily_min_spend_target on the ad set being created: the least it should spend per day, in whole currency units. A target, not a guarantee.  - It reserves a share of a CAMPAIGN budget, so it requires budgetLevel campaign or an existingCampaignId whose campaign has the budget (Advantage campaign budget / CBO). With an ad-set budget it is a 400 (Meta rejects a spend limit on an ad set that owns its budget). - Mutually exclusive with lifetimeMinSpendTarget: the flavour must match the campaign budget type. - Rejected with 400 on POST /v1/ads/boost and in adSetId attach mode: use PUT /v1/ads/ad-sets/{adSetId} for an existing ad set. | [optional]
**lifetime_min_spend_target** | Option<**f64**> | Meta lifetime_min_spend_target: the lifetime-budget flavour of dailyMinSpendTarget, in whole currency units. Same rules and same rejections. | [optional]
**customer_lifecycle** | Option<[**models::MetaCustomerLifecycle**](MetaCustomerLifecycle.md)> |  | [optional]
**ad_schedule** | Option<[**Vec<models::MetaAdScheduleInner>**](MetaAdScheduleInner.md)> | Dayparting on the ad set being created (Meta `adset_schedule` with `pacing_type: [\"day_parting\"]`). Change it later with `PUT /v1/ads/ad-sets/{adSetId}`.  A 400 with `param: platformSpecificData.adSchedule` when:  - the budget is daily (on the ad set, or on the campaign joined with `existingCampaignId`): Meta runs a schedule only on a LIFETIME budget. - the value is empty. - in adSetId attach mode. - with `buyingType: RESERVED`.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


