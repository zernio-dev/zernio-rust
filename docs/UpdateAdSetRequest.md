# UpdateAdSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **Platform** |  (enum: facebook, instagram, tiktok, linkedin, pinterest, google, twitter) | 
**budget** | Option<[**models::UpdateAdSetRequestBudget**](UpdateAdSetRequestBudget.md)> |  | [optional]
**status** | Option<**Status**> | Omit if not toggling delivery state (enum: active, paused) | [optional]
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> | Ad-set-level bid strategy. Overrides the campaign-level default. Supported on Meta (facebook, instagram) and TikTok. On TikTok the Meta-style enum is mapped to bid_type / bid_price / deep_bid_type automatically. Other platforms (linkedin, pinterest, google, twitter) return 501 Not Implemented when bidStrategy is set.  | [optional]
**bid_amount** | Option<**f64**> | Bid cap in WHOLE currency units (USD: 5 = $5.00; JPY: 100 = ¥100). Required when bidStrategy is LOWEST_COST_WITH_BID_CAP or COST_CAP. Internally converted to Meta's smallest-denomination integer.  | [optional]
**roas_average_floor** | Option<**f64**> | Minimum ROAS as a decimal multiplier (2.0 = 2.0x). Required when bidStrategy is LOWEST_COST_WITH_MIN_ROAS. Sent to Meta as `bid_constraints.roas_average_floor` × 10000.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


