# CreateRfPredictionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant). | 
**ad_account_id** | **String** | Meta ad account id (act_<n>). | 
**budget_amount** | Option<**f64**> | Whole currency units. Exactly one of budgetAmount / reach. | [optional]
**reach** | Option<**i32**> | Target unique reach. Exactly one of budgetAmount / reach. | [optional]
**start_date** | **String** | Campaign window start (must be in the future). | 
**end_date** | **String** |  | 
**frequency_cap** | Option<**i32**> | Max impressions per person over the window. | [optional]
**targeting** | Option<**serde_json::Value**> | Canonical camelCase TargetingSpec (same shape as /v1/ads/create's `targeting`). Defaults to countries: [US]. | [optional]
**placements** | Option<**serde_json::Value**> | Meta placements object (same shape as /v1/ads/create's `placements`). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


