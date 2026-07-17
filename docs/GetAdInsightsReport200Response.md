# GetAdInsightsReport200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**report_run_id** | Option<**String**> |  | [optional]
**status** | Option<**String**> | Meta async_status: Job Not Started, Job Started, Job Running, Job Completed, Job Failed, Job Skipped. | [optional]
**percent_completion** | Option<**i32**> |  | [optional]
**date_start** | Option<**String**> |  | [optional]
**date_stop** | Option<**String**> |  | [optional]
**data** | Option<**Vec<serde_json::Value>**> | Present only when status is Job Completed. | [optional]
**paging** | Option<[**models::GetAdInsightsReport200ResponsePaging**](GetAdInsightsReport200ResponsePaging.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


