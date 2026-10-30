# Cpm

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** |  (enum: cpm) | 
**metric** | Option<**Metric**> | What the rate pays on. Missing means views. (enum: views, engagements) | [optional]
**engagement_types** | Option<**Vec<EngagementTypes>**> | The engagements that count. Missing means all four. (enum: likes, comments, shares, saves) | [optional]
**rate_per1k_cents** | **i32** |  | 
**min_views_to_earn** | **i32** |  | 
**max_payout_per_clip_cents** | Option<**i32**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


