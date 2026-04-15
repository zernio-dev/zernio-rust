# SendConversions200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | Option<**Platform**> |  (enum: metaads, googleads) | [optional]
**events_received** | Option<**i32**> | Events accepted by the platform. | [optional]
**events_failed** | Option<**i32**> | Events rejected (see failures). | [optional]
**failures** | Option<[**Vec<models::SendConversions200ResponseFailuresInner>**](SendConversions200ResponseFailuresInner.md)> |  | [optional]
**trace_id** | Option<**String**> | Platform trace ID (fbtrace_id for Meta, requestId for Google) for debugging. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


