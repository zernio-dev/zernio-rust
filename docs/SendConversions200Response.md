# SendConversions200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | Option<**Platform**> |  (enum: metaads, googleads, linkedinads) | [optional]
**events_received** | Option<**i32**> | Events accepted by the platform. | [optional]
**events_failed** | Option<**i32**> | Events rejected (see failures). | [optional]
**failures** | Option<[**Vec<models::SendConversions200ResponseFailuresInner>**](SendConversions200ResponseFailuresInner.md)> |  | [optional]
**trace_id** | Option<**String**> | Platform trace ID for debugging. fbtrace_id for Meta, requestId for Google. Absent for LinkedIn (LinkedIn's conversionEvents endpoint does not surface a trace ID).  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


