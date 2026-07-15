# GetLinkedInBidPricingRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio social account ID (LinkedIn). | 
**ad_account_id** | **String** | LinkedIn ad account ID (numeric). | 
**spec** | Option<[**models::TargetingSpec**](TargetingSpec.md)> | Same targeting spec used by POST /v1/ads/create. | 
**campaign_type** | Option<**CampaignType**> | Defaults to SPONSORED_UPDATES. (enum: TEXT_AD, SPONSORED_UPDATES, SPONSORED_INMAILS) | [optional]
**bid_type** | Option<**BidType**> | Defaults to CPM. (enum: CPM, CPC, CPV) | [optional]
**match_type** | Option<**MatchType**> | Defaults to EXACT. (enum: EXACT, AUDIENCE_EXPANDED) | [optional]
**currency** | Option<**String**> | ISO 4217, defaults to USD. | [optional]
**objective_type** | Option<**String**> | LinkedIn objectiveType, e.g. WEBSITE_VISIT, LEAD_GENERATION, VIDEO_VIEW. | [optional]
**optimization_target_type** | Option<**String**> | LinkedIn optimizationTargetType, e.g. MAX_CLICK, MAX_IMPRESSION. | [optional]
**daily_budget** | Option<**f64**> | Optional daily budget in whole account-currency units. LinkedIn refines the suggested bid to this budget. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


