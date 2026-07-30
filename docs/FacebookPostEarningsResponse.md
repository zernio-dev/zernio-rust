# FacebookPostEarningsResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | Option<**bool**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**post_id** | Option<**String**> | The platform post ID that was queried, echoed back. | [optional]
**platform** | Option<**String**> |  | [optional]
**period** | Option<**Period**> | Always \"lifetime\": the total is cumulative since publication and must not be summed across dates or across posts.  (enum: lifetime) | [optional]
**metrics** | Option<[**std::collections::HashMap<String, models::FacebookPostEarningsResponseMetricsValue>**](FacebookPostEarningsResponseMetricsValue.md)> | One entry per served metric. A metric reported here with \"total\": 0 genuinely earned nothing (or its Page is not enrolled, which Meta reports identically).  | [optional]
**unavailable_metrics** | Option<[**Vec<models::FacebookPostEarningsResponseUnavailableMetricsInner>**](FacebookPostEarningsResponseUnavailableMetricsInner.md)> | Requested metrics Meta could not serve. Present only when at least one metric is unavailable, and absent otherwise. Each listed metric is OMITTED from \"metrics\" rather than reported as 0. The request itself still succeeds with HTTP 200.  | [optional]
**data_delay** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


