# CampaignResultMetric

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **String** |  | 
**label** | **String** |  | 
**kind** | **Kind** | How the value reads: `percent` values are already multiplied by 100. (enum: count, money, percent, ratio) | 
**currency** | Option<**String**> |  | 
**formula** | Option<**String**> | Null for a number you send. For a computed metric, the formula over `spend`, `impressions`, `clicks`, `conversions`, `purchase_value` and the metrics you send, e.g. `spend / revenue * 100`. | 
**built_in** | **bool** | One of the formulas every team has (`cac_percent`, `cost_per_sale`, `cost_per_qualified_lead`, `lead_to_sale`). Setting the same key replaces it for your team. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


