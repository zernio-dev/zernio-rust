# GetAdsTimeline200ResponseRowsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**date** | Option<[**String**](String.md)> |  | [optional]
**spend** | Option<**f64**> | Native currency units (matches /ads/tree convention). | [optional]
**impressions** | Option<**i32**> |  | [optional]
**reach** | Option<**i32**> |  | [optional]
**clicks** | Option<**i32**> |  | [optional]
**engagement** | Option<**i32**> |  | [optional]
**ctr** | Option<**f64**> | Click-through rate as a percentage (0–100). | [optional]
**cpc** | Option<**f64**> | Cost per click in native currency. | [optional]
**cpm** | Option<**f64**> | Cost per 1000 impressions in native currency. | [optional]
**conversions** | Option<**i32**> | Sum of conversion events matching the campaign optimization goal. Meta-only at time of writing. | [optional]
**cost_per_conversion** | Option<**f64**> |  | [optional]
**actions** | Option<**std::collections::HashMap<String, f64>**> | Per-action-type counts merged across all ads on this day. Keys are platform-native action types. | [optional]
**action_values** | Option<**std::collections::HashMap<String, f64>**> | Monetary mirror of `actions` in native currency. | [optional]
**purchase_value** | Option<**f64**> | Sum of purchase-type action values on this day, native currency. | [optional]
**roas** | Option<**f64**> | Derived purchaseValue / spend. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


