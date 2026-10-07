# UpdateAdCampaign200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**updated** | Option<**i32**> | Local Ad documents mirrored. 0 on the empty-campaign path. | [optional]
**budget** | Option<[**models::AdCampaignBudget**](AdCampaignBudget.md)> |  | [optional]
**budget_level** | Option<**BudgetLevel**> |  (enum: campaign) | [optional]
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> |  | [optional]
**bid_amount** | Option<**f64**> |  | [optional]
**roas_average_floor** | Option<**f64**> |  | [optional]
**portfolio_bid_strategy_id** | Option<**String**> | Google only. Echoed back, but NOT mirrored onto local Ad documents (no column for it yet). | [optional]
**target_impression_share** | Option<[**models::GoogleTargetImpressionShare**](GoogleTargetImpressionShare.md)> |  | [optional]
**manual_cpc** | Option<[**models::GoogleManualCpc**](GoogleManualCpc.md)> |  | [optional]
**network_settings** | Option<[**models::GoogleNetworkSettings**](GoogleNetworkSettings.md)> |  | [optional]
**tracking_url_template** | Option<**String**> |  | [optional]
**final_url_suffix** | Option<**String**> |  | [optional]
**shared_budget_id** | Option<**String**> | Google only. Echoed back when the campaign moved budgets; `budget` is then the budget it now uses. | [optional]
**platform_specific_data** | Option<**serde_json::Value**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


