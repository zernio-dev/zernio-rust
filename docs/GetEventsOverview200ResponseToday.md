# GetEventsOverview200ResponseToday

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**conversions** | Option<**i32**> | Stored events that occurred today, retracted ones excluded. | [optional]
**value** | Option<**f64**> | Value of those events in `currency`. Events in other currencies are left out. | [optional]
**currency** | Option<**String**> | The currency most of today's valued events use; `null` when none carried a value. | [optional]
**sent** | Option<**i32**> | Event sends to a destination today, one per event and destination. | [optional]
**accepted** | Option<**i32**> | Those whose latest send the platform accepted. | [optional]
**matched** | Option<**i32**> | Today's events matched to an ad campaign. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


