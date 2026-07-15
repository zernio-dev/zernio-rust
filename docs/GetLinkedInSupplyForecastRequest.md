# GetLinkedInSupplyForecastRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**ad_account_id** | **String** |  | 
**spec** | Option<[**models::TargetingSpec**](TargetingSpec.md)> |  | 
**campaign_type** | Option<**CampaignType**> | Defaults to SPONSORED_UPDATES. (enum: SPONSORED_UPDATES, SPONSORED_INMAILS, DYNAMIC) | [optional]
**time_range_start** | **i32** | Unix ms. Must be in the future. | 
**time_range_end** | **i32** | Unix ms. Must be after start and within LinkedIn's max horizon. | 
**objective_type** | Option<**String**> |  | [optional]
**optimization_target** | Option<**String**> | When set, the forecast assumes auto-bidding. When unset, competingBid is required. | [optional]
**daily_budget** | Option<**f64**> | Either dailyBudget or totalBudget is required. | [optional]
**total_budget** | Option<**f64**> |  | [optional]
**currency** | Option<**String**> | ISO 4217, defaults to USD. | [optional]
**competing_bid** | Option<[**models::GetLinkedInSupplyForecastRequestCompetingBid**](GetLinkedInSupplyForecastRequestCompetingBid.md)> |  | [optional]
**enable_audience_network** | Option<**bool**> | Defaults to false. Required true for connectedTelevisionOnly. | [optional]
**enable_audience_expansion** | Option<**bool**> | Defaults to false. | [optional]
**connected_television_only** | Option<**bool**> | Defaults to false. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


