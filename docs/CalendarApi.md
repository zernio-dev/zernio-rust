# \CalendarApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**calendar_availability**](CalendarApi.md#calendar_availability) | **POST** /v1/calendar/availability | Find meeting slots across accounts
[**calendar_free_busy**](CalendarApi.md#calendar_free_busy) | **POST** /v1/calendar/free-busy | Busy blocks for one or more accounts
[**create_calendar_event**](CalendarApi.md#create_calendar_event) | **POST** /v1/calendar/events | Create an event
[**delete_calendar_event**](CalendarApi.md#delete_calendar_event) | **DELETE** /v1/calendar/events/{eventId} | Delete an event
[**get_calendar_event**](CalendarApi.md#get_calendar_event) | **GET** /v1/calendar/events/{eventId} | Get an event
[**list_calendar_events**](CalendarApi.md#list_calendar_events) | **GET** /v1/calendar/events | List events in a window
[**list_calendars**](CalendarApi.md#list_calendars) | **GET** /v1/calendar/calendars | List calendars
[**rsvp_calendar_event**](CalendarApi.md#rsvp_calendar_event) | **POST** /v1/calendar/events/{eventId}/rsvp | Respond to an invitation
[**update_calendar_event**](CalendarApi.md#update_calendar_event) | **PATCH** /v1/calendar/events/{eventId} | Update an event



## calendar_availability

> models::CalendarAvailability200Response calendar_availability(calendar_availability_request)
Find meeting slots across accounts

Slots of `durationMinutes` every `intervalMinutes` between `from` and `to` that are free for every participant (`collective`) or for at least one (`max_availability`). Buffers pad the participants' existing meetings. Open hours are evaluated in each participant's own timezone; `defaultOpenHours` applies to participants without their own.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**calendar_availability_request** | [**CalendarAvailabilityRequest**](CalendarAvailabilityRequest.md) |  | [required] |

### Return type

[**models::CalendarAvailability200Response**](calendarAvailability_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## calendar_free_busy

> models::CalendarFreeBusy200Response calendar_free_busy(calendar_free_busy_request)
Busy blocks for one or more accounts

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**calendar_free_busy_request** | [**CalendarFreeBusyRequest**](CalendarFreeBusyRequest.md) |  | [required] |

### Return type

[**models::CalendarFreeBusy200Response**](calendarFreeBusy_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_calendar_event

> models::CreateCalendarEvent201Response create_calendar_event(create_calendar_event_request)
Create an event

`conferencing: teams` adds a Teams meeting on Microsoft accounts; the created event comes back with `conferencing: null` when the tenant has no Teams (the EEA Business Basic SKUs ship without it). `google_meet` is rejected there with 400 (`param: conferencing`). On Google accounts `conferencing: google_meet` adds a Meet link, `teams` is rejected with 400, and `recurrence` accepts any RRULE Google Calendar supports. `recurrence` takes one RRULE line with FREQ, INTERVAL, COUNT, UNTIL, BYDAY and BYSETPOS; other parts are rejected with 400 (`param: recurrence`).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_calendar_event_request** | [**CreateCalendarEventRequest**](CreateCalendarEventRequest.md) |  | [required] |

### Return type

[**models::CreateCalendarEvent201Response**](createCalendarEvent_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_calendar_event

> models::DeleteCalendarEvent200Response delete_calendar_event(event_id, account_id, calendar_id)
Delete an event

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**event_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google or Microsoft account. | [required] |
**calendar_id** | Option<**String**> | The calendar holding the event (an id from GET /v1/calendar/calendars). Defaults to the primary calendar. |  |

### Return type

[**models::DeleteCalendarEvent200Response**](deleteCalendarEvent_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_calendar_event

> models::CreateCalendarEvent201Response get_calendar_event(event_id, account_id, calendar_id, timezone)
Get an event

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**event_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google or Microsoft account. | [required] |
**calendar_id** | Option<**String**> | The calendar holding the event (an id from GET /v1/calendar/calendars). Defaults to the primary calendar. |  |
**timezone** | Option<**String**> |  |  |

### Return type

[**models::CreateCalendarEvent201Response**](createCalendarEvent_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_calendar_events

> models::ListCalendarEvents200Response list_calendar_events(account_id, from, to, calendar_id, title, location, show_cancelled, expand_recurring, ical_uid, sort_order, cursor, limit, timezone)
List events in a window

Recurring series are expanded into their occurrences inside the window by default (`expandRecurring=false` lists the masters instead). `title` and `location` are substring matches applied to the fetched page.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected Google or Microsoft account. | [required] |
**from** | **String** |  | [required] |
**to** | **String** |  | [required] |
**calendar_id** | Option<**String**> | Defaults to the primary calendar. |  |
**title** | Option<**String**> |  |  |
**location** | Option<**String**> |  |  |
**show_cancelled** | Option<**bool**> |  |  |[default to false]
**expand_recurring** | Option<**bool**> |  |  |[default to true]
**ical_uid** | Option<**String**> |  |  |
**sort_order** | Option<**String**> |  |  |[default to asc]
**cursor** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**timezone** | Option<**String**> | IANA zone the `start` and `end` offsets are rendered in. Default UTC. |  |

### Return type

[**models::ListCalendarEvents200Response**](listCalendarEvents_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_calendars

> models::ListCalendars200Response list_calendars(account_id)
List calendars

The account must have been connected with `scopes=calendar` (412 `account_scope_missing` otherwise).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected Google or Microsoft account. | [required] |

### Return type

[**models::ListCalendars200Response**](listCalendars_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## rsvp_calendar_event

> models::CreateCalendarEvent201Response rsvp_calendar_event(event_id, rsvp_calendar_event_request)
Respond to an invitation

Accepts, declines or tentatively accepts on behalf of the mailbox and notifies the organizer.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**event_id** | **String** |  | [required] |
**rsvp_calendar_event_request** | [**RsvpCalendarEventRequest**](RsvpCalendarEventRequest.md) |  | [required] |

### Return type

[**models::CreateCalendarEvent201Response**](createCalendarEvent_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_calendar_event

> models::CreateCalendarEvent201Response update_calendar_event(event_id, update_calendar_event_request)
Update an event

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**event_id** | **String** |  | [required] |
**update_calendar_event_request** | [**UpdateCalendarEventRequest**](UpdateCalendarEventRequest.md) |  | [required] |

### Return type

[**models::CreateCalendarEvent201Response**](createCalendarEvent_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

