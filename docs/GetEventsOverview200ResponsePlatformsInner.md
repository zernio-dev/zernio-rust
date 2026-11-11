# GetEventsOverview200ResponsePlatformsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> | Ad platform, such as `metaads` or `googleads`. | [optional]
**account_name** | Option<**String**> |  | [optional]
**destination_name** | Option<**String**> | The destination (pixel, dataset or conversion action) id. | [optional]
**sent_today** | Option<**i32**> | Events the platform accepted today. | [optional]
**failed_today** | Option<**i32**> | Events that failed for good today. | [optional]
**last_sent_at** | Option<**String**> | Last accepted send in the last 30 days. | [optional]
**last_event_name** | Option<**String**> | Name of the event in that send. | [optional]
**last_error** | Option<**String**> | The platform's error on the last failed send in the last 30 days. | [optional]
**fix_url** | Option<**String**> | Where to fix a failing destination. Always `null` for now. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


