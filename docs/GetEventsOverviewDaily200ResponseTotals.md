# GetEventsOverviewDaily200ResponseTotals

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**conversions** | Option<**i32**> | Stored events that occurred in the period, retracted ones excluded. | [optional]
**value** | Option<**f64**> | Value of those events in `currency`. Events in other currencies are left out. | [optional]
**value_sent** | Option<**f64**> | Value in `currency` of those events at least one platform accepted. | [optional]
**currency** | Option<**String**> | The currency most of the period's events use; `null` when none carried a value. | [optional]
**sent** | Option<**i32**> | Events first sent to a destination in the period, one per event and destination. | [optional]
**accepted** | Option<**i32**> | Those whose latest send the platform accepted. | [optional]
**matched** | Option<**i32**> | The period's events matched to an ad campaign. | [optional]
**counted** | Option<**i32**> | The period's events that count as campaign results, the ones looked up for a campaign. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


