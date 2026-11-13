# ListCalendarEvents200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | Option<[**Vec<models::CalendarEvent>**](CalendarEvent.md)> |  | [optional]
**pagination** | Option<[**models::CursorPagination**](CursorPagination.md)> |  | [optional]
**stale** | Option<**bool**> | Always true when present. Present only when the provider did not answer and this is the last list Zernio read for the same account and query within the past six hours. | [optional]
**as_of** | Option<**String**> | When a stale list was read from the provider. Present only with `stale`. | [optional]
**partial** | Option<**bool**> | Always true when present. This response is one slice of the requested window because the provider did not answer for the whole of it. Follow `pagination.nextCursor` until it is null. Present only on a degraded read. | [optional]
**covered_from** | Option<**String**> | Start of the part of the window this slice covers. Present only with `partial`. | [optional]
**covered_to** | Option<**String**> | End of the part of the window this slice covers. Present only with `partial`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


