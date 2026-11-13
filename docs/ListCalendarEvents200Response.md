# ListCalendarEvents200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | Option<[**Vec<models::CalendarEvent>**](CalendarEvent.md)> |  | [optional]
**pagination** | Option<[**models::CursorPagination**](CursorPagination.md)> |  | [optional]
**stale** | Option<**bool**> | Always true when present. Present only when the provider did not answer and this is the last list Zernio read for the same account and query within the past hour. | [optional]
**as_of** | Option<**String**> | When a stale list was read from the provider. Present only with `stale`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


