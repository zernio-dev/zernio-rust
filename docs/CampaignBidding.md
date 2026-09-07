# CampaignBidding

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel** | Option<**Channel**> | campaign.advertising_channel_type. COST_CAP's underlying Google field differs by channel; see bidStrategy on PUT. (enum: SEARCH, DISPLAY) | [optional]
**bidding_strategy_type** | Option<**String**> | Google's raw enum: MAXIMIZE_CONVERSIONS, TARGET_CPA, MAXIMIZE_CONVERSION_VALUE, TARGET_ROAS, TARGET_SPEND, MANUAL_CPC, TARGET_IMPRESSION_SHARE, or another Google adds later. | [optional]
**bid_spec** | Option<[**models::CampaignBiddingBidSpec**](CampaignBiddingBidSpec.md)> |  | [optional]
**portfolio** | Option<[**models::CampaignBiddingPortfolio**](CampaignBiddingPortfolio.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


