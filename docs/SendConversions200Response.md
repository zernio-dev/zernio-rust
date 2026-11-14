# SendConversions200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | Option<**Platform**> |  (enum: metaads, googleads, linkedinads, tiktokads, openaiads, pinterestads, redditads) | [optional]
**events_received** | Option<**i32**> | Events accepted by the platform. | [optional]
**events_failed** | Option<**i32**> | Events rejected (see failures). | [optional]
**failures** | Option<[**Vec<models::SendConversions200ResponseFailuresInner>**](SendConversions200ResponseFailuresInner.md)> |  | [optional]
**trace_id** | Option<**String**> | Platform trace ID for debugging. fbtrace_id for Meta, requestId for Google, request_id for TikTok. Absent for LinkedIn (LinkedIn's conversionEvents endpoint does not surface a trace ID), OpenAI Ads and Reddit (no trace ID surfaced).  | [optional]
**platform_messages** | Option<**Vec<String>**> | Meta only. Meta's `messages` (warnings about the events it accepted), each distinct one once, at most 20. Absent when Meta sent none. | [optional]
**test_code** | Option<**String**> | The test code sent to the platform, as received (from `testCode` or `test_event_code`). `null` when the request carried none, so the events were sent as production events. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


