# SendEvents200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**events_received** | Option<**i32**> | Events in the request. | [optional]
**stored** | Option<**bool**> | Whether the events were stored for reporting (always false with testCode). | [optional]
**test_code** | Option<**String**> | The test code forwarded to every destination, or `null` when the request carried none. | [optional]
**destinations** | Option<[**Vec<models::SendEvents200ResponseDestinationsInner>**](SendEvents200ResponseDestinationsInner.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


