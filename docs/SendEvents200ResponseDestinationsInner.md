# SendEvents200ResponseDestinationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> |  | [optional]
**destination_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: metaads, googleads, linkedinads, tiktokads, openaiads, pinterestads, redditads) | [optional]
**events_sent** | Option<**i32**> | Events the platform accepted. | [optional]
**events_failed** | Option<**i32**> |  | [optional]
**failures** | Option<[**Vec<models::SendEvents200ResponseDestinationsInnerFailuresInner>**](SendEvents200ResponseDestinationsInnerFailuresInner.md)> |  | [optional]
**error** | Option<**String**> | Set when the destination could not be reached at all (account disconnected, unsupported platform, platform error). | [optional]
**retrying** | Option<**bool**> | The destination failed for now (platform error, timeout, rate limit) and the send is queued for retries; its outcome shows on GET /v1/events/{eventId}. | [optional]
**trace_id** | Option<**String**> | The platform trace ID of the send (Meta `fbtrace_id`, Google `requestId`, TikTok `request_id`), to quote to the platform support. Absent when the platform returns none. | [optional]
**platform_messages** | Option<**Vec<String>**> | Meta's `messages` (warnings about the events it accepted), each distinct one once, at most 20. Absent when the platform sent none. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


