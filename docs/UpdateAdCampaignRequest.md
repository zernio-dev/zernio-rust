# UpdateAdCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **Platform** | Required: platform campaign IDs are not globally unique. (enum: facebook, instagram, google) | 
**account_id** | Option<**String**> | **Meta only.** Zernio SocialAccount id owning the ad account. Needed only for an EMPTY campaign (zero ads); ignored otherwise. | [optional]
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> | **Meta + Google.** On Meta, the campaign default that ad sets inherit unless they override it. On Google, the campaign's own bidding strategy. On Google: LOWEST_COST_WITHOUT_CAP = Maximize Conversions, COST_CAP + bidAmount = Target CPA, LOWEST_COST_WITH_MIN_ROAS + roasAverageFloor = Target ROAS, LOWEST_COST_WITH_BID_CAP + bidAmount = Maximize Clicks with a CPC ceiling; portfolioBidStrategyId attaches a portfolio strategy instead. | [optional]
**bid_amount** | Option<**f64**> | **Google only.** Whole currency units (USD: 12 = $12.00). Max CPC for LOWEST_COST_WITH_BID_CAP, CPA target for COST_CAP; required for both. | [optional]
**roas_average_floor** | Option<**f64**> | **Google only.** Decimal ROAS multiplier (2.0 = 2.0x), required for LOWEST_COST_WITH_MIN_ROAS. | [optional]
**portfolio_bid_strategy_id** | Option<**String**> | **Google only.** Attach an existing portfolio bid strategy (numeric id from GET /v1/ads/bid-strategies) instead of setting bidStrategy. Exclusive with bidStrategy. | [optional]
**allow_shared_budget_update** | Option<**bool**> | Google only. Explicitly allow changing a shared campaign budget, affecting every campaign that uses it. Does not bypass an unknown sharing state. | [optional][default to false]
**budget** | Option<[**models::UpdateAdCampaignRequestBudget**](UpdateAdCampaignRequestBudget.md)> |  | [optional]
**name** | Option<**String**> | **Meta only.** Rename the campaign. | [optional]
**platform_specific_data** | Option<[**models::UpdateAdCampaignRequestPlatformSpecificData**](UpdateAdCampaignRequestPlatformSpecificData.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


