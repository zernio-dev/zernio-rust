# ListWhatsAppConversions200ResponseEventsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | Option<**String**> | When the event was sent to Meta. | [optional]
**event_name** | Option<**String**> | One of LeadSubmitted, Purchase, AddToCart, InitiateCheckout, ViewContent. | [optional]
**conversation_id** | Option<**String**> |  | [optional]
**events_received** | Option<**i32**> | Number of events Meta accepted on this send (usually 1). | [optional]
**events_failed** | Option<**i32**> | Number of events Meta rejected (usually 0). | [optional]
**trace_id** | Option<**String**> | Meta fbtrace_id for cross-referencing in Events Manager. | [optional]
**duration_ms** | Option<**i32**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


