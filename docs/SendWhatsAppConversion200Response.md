# SendWhatsAppConversion200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | Option<**Platform**> |  (enum: metaads) | [optional]
**events_received** | Option<**i32**> | Events accepted by Meta. | [optional]
**events_failed** | Option<**i32**> | Events rejected by Meta (see failures). | [optional]
**failures** | Option<[**Vec<models::SendConversions200ResponseFailuresInner>**](SendConversions200ResponseFailuresInner.md)> | Per-event failure detail. Empty when all events were accepted.  | [optional]
**trace_id** | Option<**String**> | Meta `fbtrace_id` for debugging. Surface in support tickets.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


