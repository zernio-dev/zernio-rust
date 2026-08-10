# MetaAdsPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> |  | [optional]
**bid_amount** | Option<**f64**> | Whole currency units (USD: 5 = $5.00). Required when bidStrategy is LOWEST_COST_WITH_BID_CAP or COST_CAP. May also be sent alone, WITHOUT bidStrategy, to set the cap on an ad set joining a COST_CAP / LOWEST_COST_WITH_BID_CAP campaign (the strategy is inherited from the campaign). On POST /v1/ads/create that shape requires existingCampaignId and is a 400 otherwise; on POST /v1/ads/boost it is promoted to LOWEST_COST_WITH_BID_CAP. | [optional]
**roas_average_floor** | Option<**f64**> | Decimal ROAS multiplier (2.0 = 2.0x). Required when bidStrategy is LOWEST_COST_WITH_MIN_ROAS; sending it without bidStrategy is a 400. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


