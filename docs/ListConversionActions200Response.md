# ListConversionActions200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customer_id** | Option<**String**> | The Google Ads customer id the actions were read from. | [optional]
**actions** | Option<[**Vec<models::ConversionAction>**](ConversionAction.md)> |  | [optional]
**cached_at** | Option<**String**> | When this list was fetched from Google. Null when it was never served from cache. | [optional]
**stale** | Option<**bool**> | True when Google's daily API quota was exhausted and this is the last successful fetch, not a live read. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


