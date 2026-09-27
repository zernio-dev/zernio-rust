# ListAdLabels200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_account_id** | Option<**String**> | Meta act_<n>, or the resolved Google customer id | [optional]
**data** | Option<[**Vec<models::ListAdLabels200ResponseDataInner>**](ListAdLabels200ResponseDataInner.md)> |  | [optional]
**paging** | Option<[**models::ListAdLabels200ResponsePaging**](ListAdLabels200ResponsePaging.md)> |  | [optional]
**cached_at** | Option<**String**> | Google only. When the served list was fetched from Google. | [optional]
**stale** | Option<**bool**> | Google only. True when Google quota was exhausted and the last cached list was served. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


