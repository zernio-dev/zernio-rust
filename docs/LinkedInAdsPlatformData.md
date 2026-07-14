# LinkedInAdsPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cost_type** | Option<**CostType**> | Campaign cost model (billing event). Defaults to `CPM`. Required when `unitCost` is set so the manual bid applies to an explicit cost model.  (enum: CPM, CPC, CPV) | [optional]
**unit_cost** | Option<**f64**> | Manual bid in WHOLE account-currency units (e.g. 2.5 = $2.50). Requires `costType`. Omit for LinkedIn's automated (max delivery) bidding. LinkedIn enforces its own per-audience min/max bid bounds.  | [optional]
**optimization_target_type** | Option<**String**> | Campaign `optimizationTargetType` (e.g. `MAX_CLICK`, `TARGET_COST_PER_CLICK`, `MAX_IMPRESSION`). Forwarded verbatim — LinkedIn validates compatibility with the objective and `costType`. Omit for the objective-derived default.  | [optional]
**creative_selection** | Option<**CreativeSelection**> | How LinkedIn rotates creatives within the campaign. Defaults to `OPTIMIZED`. (enum: OPTIMIZED, ROUND_ROBIN) | [optional]
**audience_expansion_enabled** | Option<**bool**> | Enable LinkedIn audience expansion. Defaults to false. | [optional]
**offsite_delivery_enabled** | Option<**bool**> | Deliver on the LinkedIn Audience Network. Defaults to false. | [optional]
**connected_television_only** | Option<**bool**> | Restrict delivery to Connected TV inventory. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


