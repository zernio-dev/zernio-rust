# GetEventsOverviewDaily200ResponseDaysInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**day** | Option<[**String**](String.md)> |  | [optional]
**conversions** | Option<**i32**> | Stored events that occurred that day. | [optional]
**sent** | Option<**i32**> | Events first sent to a destination that day. | [optional]
**accepted** | Option<**i32**> | Those the platform accepted. | [optional]
**value** | Option<**f64**> | The day's value, in the period's `totals.currency`. | [optional]
**value_sent** | Option<**f64**> | Of that value, the conversions a platform accepted. | [optional]
**from_ads** | Option<**i32**> | Counted events that came from an ad, as in `totals.fromAds`. | [optional]
**matched** | Option<**i32**> | Events matched to an ad campaign. | [optional]
**by_event** | Option<**std::collections::HashMap<String, i32>**> | The day's stored events per event name. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


