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
**allow_shared_budget_update** | Option<**bool**> | Google only. Explicitly allow changing a shared campaign budget (flagged as shared by Google, or used by more than one campaign), affecting every campaign that uses it. Does not bypass an unknown sharing state. Also required to move a campaign onto a shared budget with sharedBudgetId. | [optional][default to false]
**target_impression_share** | Option<[**models::GoogleTargetImpressionShare**](GoogleTargetImpressionShare.md)> | Google Search only. Target impression share bidding. Exclusive with bidStrategy, portfolioBidStrategyId and manualCpc; bidAmount is refused alongside it (the ceiling is maxCpc). | [optional]
**manual_cpc** | Option<[**models::GoogleManualCpc**](GoogleManualCpc.md)> |  | [optional]
**network_settings** | Option<[**models::GoogleNetworkSettings**](GoogleNetworkSettings.md)> |  | [optional]
**tracking_url_template** | Option<**String**> | **Google only.** campaign.tracking_url_template; an empty string clears it. | [optional]
**final_url_suffix** | Option<**String**> | **Google only.** campaign.final_url_suffix; an empty string clears it. | [optional]
**shared_budget_id** | Option<**String**> | **Google only.** Move the campaign onto this shared budget (id from GET /v1/ads/shared-budgets), or null to move it back onto a budget of its own sized by `budget`. | [optional]
**budget** | Option<[**models::UpdateAdCampaignRequestBudget**](UpdateAdCampaignRequestBudget.md)> |  | [optional]
**name** | Option<**String**> | **Meta only.** Rename the campaign. | [optional]
**platform_specific_data** | Option<[**models::UpdateAdCampaignRequestPlatformSpecificData**](UpdateAdCampaignRequestPlatformSpecificData.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


