# GetAdsTimeline202Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**backfill_pending** | **bool** | Always true on this response. Part of the requested range is still being backfilled; retry until the request returns 200. | 
**previous_rows** | Option<**Vec<std::collections::HashMap<String, serde_json::Value>>**> | Only with `compare=previous`. The daily rows of `previousRange`, in the same shape as `rows`. | [optional]
**previous_range** | Option<[**models::AdsTimelineResponsePreviousRange**](AdsTimelineResponsePreviousRange.md)> |  | [optional]
**rows** | Option<[**Vec<models::AdsTimelineResponseRowsInner>**](AdsTimelineResponseRowsInner.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


