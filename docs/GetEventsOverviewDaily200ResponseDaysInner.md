# GetEventsOverviewDaily200ResponseDaysInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**day** | Option<[**String**](String.md)> |  | [optional]
**conversions** | Option<**i32**> | Stored events that occurred that day. | [optional]
**sent** | Option<**i32**> | Events first sent to a destination that day. | [optional]
**accepted** | Option<**i32**> | Those the platform accepted. | [optional]
**by_event** | Option<**std::collections::HashMap<String, i32>**> | The day's stored events per event name. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


