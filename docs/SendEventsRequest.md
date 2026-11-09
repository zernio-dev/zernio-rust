# SendEventsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** | Profile the events belong to. Its saved destinations receive the events. | 
**events** | [**Vec<models::ConversionEvent>**](ConversionEvent.md) |  | 
**destinations** | Option<[**Vec<models::SendEventsRequestDestinationsInner>**](SendEventsRequestDestinationsInner.md)> | Send to these destinations instead of the saved ones (every event goes to each). | [optional]
**consent** | Option<[**models::SendEventsRequestConsent**](SendEventsRequestConsent.md)> |  | [optional]
**test_code** | Option<**String**> | Forwarded as each platform test code (see POST /v1/ads/conversions). A root-level `test_event_code` is accepted as an alias. Test events are not stored. | [optional]
**mode** | Option<**Mode**> | `sync` sends to every destination before answering (200, per-destination results). `async` stores and queues the sends, then answers 202 at once; each send is retried while the platform fails for now, and its outcome shows on GET /v1/events/{eventId}. Requests with `testCode` always send now. (enum: sync, async) | [optional][default to Sync]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


