# PortfolioBidStrategy

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Numeric bid strategy id; pass as portfolioBidStrategyId or in the {strategyId} path. | [optional]
**name** | Option<**String**> |  | [optional]
**r#type** | Option<**Type**> |  (enum: TARGET_CPA, TARGET_ROAS, MAXIMIZE_CONVERSIONS, MAXIMIZE_CONVERSION_VALUE) | [optional]
**status** | Option<**String**> | ENABLED or REMOVED. | [optional]
**campaign_count** | Option<**i32**> | Number of campaigns currently attached. | [optional]
**clicks** | Option<**i32**> |  | [optional]
**cost** | Option<**f64**> | Cost in the account's currency units (converted from micros). | [optional]
**cost_per_conversion** | Option<**f64**> | Cost per conversion in the account's currency units. | [optional]
**impressions** | Option<**i32**> |  | [optional]
**average_cpc** | Option<**f64**> | Average CPC in the account's currency units. | [optional]
**conversions** | Option<**f64**> |  | [optional]
**target_cpa** | Option<**f64**> | Current target, in the account's currency units. Null for a ROAS-family type (TARGET_ROAS, MAXIMIZE_CONVERSION_VALUE), or a Maximize type with no target set. Pre-fills the edit form's target field. | [optional]
**target_roas** | Option<**f64**> | Current target as a decimal multiplier (2.0 = 2.0x). Null for a CPA-family type (TARGET_CPA, MAXIMIZE_CONVERSIONS), or a Maximize type with no target set. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


