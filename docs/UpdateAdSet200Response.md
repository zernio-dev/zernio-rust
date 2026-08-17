# UpdateAdSet200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**budget** | Option<[**models::AdBudget**](AdBudget.md)> |  | [optional]
**budget_level** | Option<**BudgetLevel**> |  (enum: adset) | [optional]
**status** | Option<**Status**> | The status written to the ad set. Absent when nothing was written (see statusMessage). (enum: active, paused) | [optional]
**status_updated** | Option<**i32**> | Number of ads whose own stored status changed alongside the ad set switch | [optional]
**status_skipped** | Option<**i32**> | Number of ads whose own status was left as it was | [optional]
**status_skipped_reasons** | Option<**Vec<String>**> | Why each group of ads was skipped | [optional]
**status_message** | Option<**String**> | Present only where the platform has no ad-set switch and no child ad was actionable; `status` is then absent because nothing was written | [optional]
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> |  | [optional]
**bid_amount** | Option<**f64**> |  | [optional]
**roas_average_floor** | Option<**f64**> |  | [optional]
**platform_specific_data** | Option<**serde_json::Value**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


