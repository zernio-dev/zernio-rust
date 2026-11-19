# PostMetricFormat

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**format** | **Format** | gif counts as image, document as text. (enum: image, video, carousel, text) | 
**post_count** | **i32** | Posts of the format published in the range. | 
**metrics** | **std::collections::HashMap<String, f64>** | Each metric asked, summed over the newest posts of the range up to meta.metricsSample.limit; engagementRate pools them. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


