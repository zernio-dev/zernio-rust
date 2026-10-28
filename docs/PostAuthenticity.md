# PostAuthenticity

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**post_id** | **String** | The external post the score belongs to | 
**score** | **i32** | Higher means the view pattern looks more organic | 
**confidence** | **f64** | How much data the score rests on | 
**reasons** | [**Vec<models::PostAuthenticityReasonsInner>**](PostAuthenticityReasonsInner.md) | Each factor that lowered the score, with its weight in points | 
**version** | **String** | Scoring model version | 
**computed_at** | **String** |  | 
**sample_count** | **i32** | Number of samples the score was computed from | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


