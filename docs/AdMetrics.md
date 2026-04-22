# AdMetrics

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**spend** | Option<**f64**> |  | [optional]
**impressions** | Option<**i32**> |  | [optional]
**reach** | Option<**i32**> |  | [optional]
**clicks** | Option<**i32**> |  | [optional]
**ctr** | Option<**f64**> | Click-through rate (%) | [optional]
**cpc** | Option<**f64**> | Cost per click | [optional]
**cpm** | Option<**f64**> | Cost per 1000 impressions | [optional]
**engagement** | Option<**i32**> |  | [optional]
**conversions** | Option<**i32**> | Count of conversion events matching the campaign's promoted_object.custom_event_type (PURCHASE, LEAD, etc.) over the requested date range. 0 for non-conversion campaigns or when no events have fired. Meta-only at time of writing; other platforms return 0. | [optional]
**cost_per_conversion** | Option<**f64**> | Derived spend / conversions in the same currency as spend. 0 when conversions is 0. | [optional]
**actions** | Option<**std::collections::HashMap<String, i32>**> | Raw per-action-type counts from Meta's Insights actions[] array, summed over the date range. Keys are Meta action_type strings (e.g. link_click, offsite_conversion.fb_pixel_purchase, onsite_conversion.lead_grouped). Use this to extract any conversion event (purchases, leads, add_to_cart, etc.) without relying on the derived conversions field. Empty object when no actions are reported. | [optional]
**action_values** | Option<**std::collections::HashMap<String, f64>**> | Monetary mirror of `actions`, from Meta's Insights `action_values[]` array. Same keying — values are the revenue attributed to each action_type, in ad-account native currency (same unit as `spend`; see the campaign node's `currency` field). Use this to compute revenue-per-event (e.g. avg purchase value). Meta-only; other platforms return {}. | [optional]
**purchase_value** | Option<**f64**> | Convenience sum of purchase-type action values — picked from `actionValues` via the same priority list as `conversions` so both fields describe the same events. In ad-account native currency. 0 when the campaign has no purchase event configured. Meta-only. | [optional]
**roas** | Option<**f64**> | Return on ad spend — derived as `purchaseValue / spend`. 0 when `spend` is 0. Equivalent to Meta's `purchase_roas` under default attribution. At ad-set and campaign levels this is recomputed from summed purchaseValue + spend (NOT averaged across children) so it's mathematically correct at every rollup level. | [optional]
**last_synced_at** | Option<**String**> | Present on individual ads only, not on campaign aggregations | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


