# InsightRetentionCurve

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**from_date** | **String** | fromDate when given; otherwise the publish date, so the curve covers the video lifetime. | 
**to_date** | **String** |  | 
**provisional_since** | Option<**String**> |  | 
**duration_seconds** | Option<**f64**> |  | 
**segment_metrics_available** | **bool** | False when YouTube has no startedWatching and stoppedWatching for the video; they read 0. | 
**points** | [**Vec<models::InsightRetentionPoint>**](InsightRetentionPoint.md) | Up to 100 points, ascending; empty when YouTube has no curve, as on videos with very few views. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


