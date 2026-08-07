# UpdateAdCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **Platform** | Required: platform campaign IDs are not globally unique. (enum: facebook, instagram, google) | 
**account_id** | Option<**String**> | **Meta only.** Zernio SocialAccount id owning the ad account. Needed only for an EMPTY campaign (zero ads); ignored otherwise. | [optional]
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> | **Meta + Google.** On Meta, the campaign default that ad sets inherit unless they override it. On Google, the campaign's own bidding strategy. | [optional]
**bid_amount** | Option<**f64**> | **Google only.** Whole currency units (USD: 12 = $12.00). Max CPC for LOWEST_COST_WITH_BID_CAP, CPA target for COST_CAP; required for both. | [optional]
**roas_average_floor** | Option<**f64**> | **Google only.** Decimal ROAS multiplier (2.0 = 2.0x), required for LOWEST_COST_WITH_MIN_ROAS. | [optional]
**budget** | Option<[**models::UpdateAdCampaignRequestBudget**](UpdateAdCampaignRequestBudget.md)> |  | [optional]
**name** | Option<**String**> | **Meta only.** Rename the campaign. | [optional]
**platform_specific_data** | Option<[**models::UpdateAdCampaignRequestPlatformSpecificData**](UpdateAdCampaignRequestPlatformSpecificData.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


