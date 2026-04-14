# AdTreeAdSet

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform_ad_set_id** | Option<**String**> |  | [optional]
**ad_set_name** | Option<**String**> |  | [optional]
**status** | Option<**Status**> | Derived from child ad statuses (enum: active, paused, pending_review, rejected, completed, cancelled, error) | [optional]
**ad_count** | Option<**i32**> |  | [optional]
**budget** | Option<[**models::AdBudget**](AdBudget.md)> |  | [optional]
**metrics** | Option<[**models::AdMetrics**](AdMetrics.md)> |  | [optional]
**optimization_goal** | Option<**String**> | Meta ad set optimization goal (e.g. OFFSITE_CONVERSIONS, VALUE, LEAD_GENERATION) | [optional]
**bid_strategy** | Option<**String**> | Bid strategy for this ad set (overrides campaign level when set) | [optional]
**promoted_object** | Option<[**models::AdTreeAdSetPromotedObject**](AdTreeAdSetPromotedObject.md)> |  | [optional]
**ads** | Option<[**Vec<models::Ad>**](Ad.md)> | Individual ads within this ad set (capped at 100). Returns a subset of Ad fields from the aggregation (core fields like _id, name, platform, status, budget, metrics, creative, goal are included; targeting and schedule may be absent). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


