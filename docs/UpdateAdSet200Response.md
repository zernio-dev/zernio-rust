# UpdateAdSet200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**budget** | Option<[**models::AdBudget**](AdBudget.md)> |  | [optional]
**budget_level** | Option<**BudgetLevel**> |  (enum: adset) | [optional]
**status** | Option<**Status**> | As in PUT /v1/ads/ad-sets/{adSetId}/status: delivery derived from the switches read back. (enum: active, paused) | [optional]
**platform_ad_set_status** | Option<**String**> | The ad set's status read back from the platform, as in PUT /v1/ads/ad-sets/{adSetId}/status (Meta and Reddit return the ad set's effective_status); null when it could not be read. | [optional]
**platform_campaign_status** | Option<**String**> |  | [optional]
**status_read_at** | Option<**String**> |  | [optional]
**status_updated** | Option<**StatusUpdated**> | 1 when the ad set's switch was written. (enum: 0, 1) | [optional]
**status_skipped** | Option<**StatusSkipped**> | 1 when a live read showed it already in the requested state. (enum: 0, 1) | [optional]
**status_skipped_reasons** | Option<**Vec<String>**> |  | [optional]
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> |  | [optional]
**bid_amount** | Option<**f64**> |  | [optional]
**roas_average_floor** | Option<**f64**> |  | [optional]
**platform_specific_data** | Option<**serde_json::Value**> |  | [optional]
**targeting** | Option<**serde_json::Value**> | Present when `placements` or `targeting` was sent. The ad set's full Meta targeting as written (Meta snake_case). The same snake_case object is stored as the ad set's and its ads' `targeting`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


