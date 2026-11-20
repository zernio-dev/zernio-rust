# MetaAdsPlatformQueryBody

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio id of the connected Meta ads account. | 
**ad_account_id** | **String** | The Meta ad account, act_<n>. Read its campaigns, ad sets or ads with level and filtering. | 
**level** | Option<**Level**> | The level of each row. Defaults to the ad account. (enum: ad, adset, campaign, account) | [optional]
**fields** | Option<**Vec<String>**> | Meta insights fields, such as spend or impressions, up to 100. | [optional]
**breakdowns** | Option<**Vec<String>**> | Meta breakdowns, up to 5. | [optional]
**action_breakdowns** | Option<**Vec<String>**> | An empty array asks Meta for no action breakdown at all. | [optional]
**action_attribution_windows** | Option<**Vec<String>**> | Meta attribution windows, such as 7d_click or 1d_view. | [optional]
**action_report_time** | Option<**String**> | impression, conversion or mixed. | [optional]
**use_unified_attribution_setting** | Option<**bool**> | Use each ad set's own attribution setting. | [optional]
**filtering** | Option<[**Vec<models::MetaAdsPlatformQueryBodyFilteringInner>**](MetaAdsPlatformQueryBodyFilteringInner.md)> | Meta filters of field, operator and value, up to 25. | [optional]
**date_preset** | Option<**String**> | A Meta date preset, such as last_30d. Not with fromDate and toDate. | [optional]
**from_date** | Option<[**String**](String.md)> | First day, YYYY-MM-DD, sent with toDate. | [optional]
**to_date** | Option<[**String**](String.md)> | Last day, YYYY-MM-DD, sent with fromDate. | [optional]
**time_increment** | Option<[**models::MetaAdsPlatformQueryBodyTimeIncrement**](MetaAdsPlatformQueryBodyTimeIncrement.md)> |  | [optional]
**limit** | Option<**i32**> | Rows per page, up to 500. Defaults to 500. | [optional][default to 500]
**cursor** | Option<**String**> | The pagination.nextCursor of the previous page, unchanged. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


