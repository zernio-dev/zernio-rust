# CalendarFreeBusy200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> |  | [optional]
**from** | Option<**String**> |  | [optional]
**to** | Option<**String**> |  | [optional]
**busy** | Option<[**Vec<models::BusyBlock>**](BusyBlock.md)> | The account's own busy time across the calendars read, merged. Null when the account could not be read. | [optional]
**calendars** | Option<[**Vec<models::CalendarFreeBusy200ResponseDataInnerCalendarsInner>**](CalendarFreeBusy200ResponseDataInnerCalendarsInner.md)> |  | [optional]
**people** | Option<[**Vec<models::CalendarFreeBusy200ResponseDataInnerPeopleInner>**](CalendarFreeBusy200ResponseDataInnerPeopleInner.md)> |  | [optional]
**error** | Option<[**models::FreeBusyError**](FreeBusyError.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


