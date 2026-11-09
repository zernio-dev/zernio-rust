# SendEvents202Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**events_received** | Option<**i32**> |  | [optional]
**stored** | Option<**bool**> |  | [optional]
**queued_destinations** | Option<**i32**> | Destinations whose sends were queued. | [optional]
**destinations** | Option<**Vec<serde_json::Value>**> |  | [optional]
**test_code** | Option<**String**> | Always `null`: requests with a test code send now and answer 200. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


