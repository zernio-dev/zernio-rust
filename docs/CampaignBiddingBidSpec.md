# CampaignBiddingBidSpec

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> |  | [optional]
**bid_amount** | Option<**f64**> | Whole currency units. Present for COST_CAP and LOWEST_COST_WITH_BID_CAP, and omitted when the campaign is on a bare TARGET_SPEND with no CPC ceiling set. | [optional]
**roas_average_floor** | Option<**f64**> | Decimal ROAS multiplier (2.0 = 2.0x). Present for LOWEST_COST_WITH_MIN_ROAS. | [optional]
**portfolio_bid_strategy_id** | Option<**String**> | Present alone (bidStrategy omitted) when the campaign is on a portfolio strategy; see portfolio. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


