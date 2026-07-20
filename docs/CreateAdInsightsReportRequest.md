# CreateAdInsightsReportRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant). | 
**object_id** | **String** | Meta insights node: act_<n>, campaign id, ad set id or ad id. | 
**level** | Option<**Level**> |  (enum: ad, adset, campaign, account) | [optional]
**fields** | Option<**String**> | Comma-separated Graph insights fields. | [optional]
**breakdowns** | Option<**String**> | Comma-separated Graph breakdowns. | [optional]
**action_breakdowns** | Option<**String**> | Comma-separated Graph action breakdowns (e.g. action_type,action_destination). | [optional]
**action_attribution_windows** | Option<**Vec<String>**> | Meta attribution windows (e.g. [\"7d_click\", \"1d_view\"]). Action values are returned keyed per window. | [optional]
**action_report_time** | Option<**String**> | When actions are counted: impression, conversion or mixed. | [optional]
**use_unified_attribution_setting** | Option<**bool**> | Use the ad sets' own attribution settings for action counting. | [optional]
**filtering** | Option<[**Vec<models::CreateAdInsightsReportRequestFilteringInner>**](CreateAdInsightsReportRequestFilteringInner.md)> | Meta filter objects, applied server-side. | [optional]
**date_preset** | Option<**String**> | Mutually exclusive with fromDate/toDate. | [optional]
**from_date** | Option<[**String**](String.md)> |  | [optional]
**to_date** | Option<[**String**](String.md)> |  | [optional]
**time_increment** | Option<[**models::CreateAdInsightsReportRequestTimeIncrement**](CreateAdInsightsReportRequestTimeIncrement.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


