# CreatorCampaignEconomicsCpm

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** |  (enum: cpm) | 
**metric** | Option<**Metric**> | What the rate pays on. `engagements` counts the `engagementTypes` as each platform reports them, and `minViewsToEarn` then applies to engagements. Fixed once the campaign leaves draft. (enum: views, engagements) | [optional][default to Views]
**engagement_types** | Option<**Vec<EngagementTypes>**> | With `metric: engagements`, the engagements that count. Missing means all four, and sending it on a views campaign answers 400. YouTube reports likes and comments only, Facebook and Threads have no saves, and Pinterest reports saves only. (enum: likes, comments, shares, saves) | [optional]
**rate_per1k_cents** | **i32** |  | 
**min_views_to_earn** | **i32** | The count a post must reach before it earns, in the campaign metric (views or engagements). | 
**max_payout_per_clip_cents** | Option<**i32**> |  | [optional]
**budget_cents** | **i32** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


