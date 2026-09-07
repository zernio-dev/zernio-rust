# ListBidStrategies200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customer_id** | Option<**String**> |  | [optional]
**currency** | Option<**String**> | Account currency code; money fields are in this currency's units. | [optional]
**strategies** | Option<[**Vec<models::PortfolioBidStrategy>**](PortfolioBidStrategy.md)> |  | [optional]
**cached_at** | Option<**String**> | When this data was fetched from Google. Null when it was never served from cache. | [optional]
**stale** | Option<**bool**> | True when Google's daily API quota was exhausted and this is the last successful fetch, not a live read. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


