# PostMetricSlot

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**day_of_week** | **i32** | UTC weekday the posts were published, 1 (Monday) to 7. | 
**hour** | **i32** | UTC hour the posts were published, 0 to 23. | 
**post_count** | **i32** | Posts published in the slot that have been synced at least once. | 
**metrics** | **std::collections::HashMap<String, f64>** | Each metric asked, summed over each post's latest snapshot; engagementRate pools them. null when no platform of the slot reports it. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


