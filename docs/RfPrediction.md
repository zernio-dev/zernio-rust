# RfPrediction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**prediction_id** | Option<**String**> |  | [optional]
**status** | Option<**String**> | ready | pending | failed:<meta code> | [optional]
**budget** | Option<**f64**> | Quoted (or provided) lifetime budget for the window. | [optional]
**reach** | Option<**i32**> | Predicted (or requested) unique reach. | [optional]
**impressions** | Option<**i32**> |  | [optional]
**min_budget** | Option<**f64**> | Meta's allowed lower bound for this spec. | [optional]
**max_budget** | Option<**f64**> |  | [optional]
**min_reach** | Option<**i32**> |  | [optional]
**max_reach** | Option<**i32**> |  | [optional]
**frequency_cap** | Option<**i32**> |  | [optional]
**start_time** | Option<**i32**> | Unix seconds; the reserved window the R&F ad set will run on. | [optional]
**stop_time** | Option<**i32**> |  | [optional]
**expires_at** | Option<**String**> | When the reservation's locked price expires (set after reserving). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


