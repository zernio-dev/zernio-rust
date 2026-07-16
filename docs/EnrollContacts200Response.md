# EnrollContacts200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | Option<**bool**> |  | [optional]
**enrolled** | Option<**i32**> | Number of contacts successfully enrolled | [optional]
**failed** | Option<**i32**> | Number that failed (already enrolled, or no subscribed channel on the sequence platform) | [optional]
**results** | Option<[**Vec<models::EnrollContacts200ResponseResultsInner>**](EnrollContacts200ResponseResultsInner.md)> | Per-contact outcome | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


