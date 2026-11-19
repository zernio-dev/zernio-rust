# MetricEntity

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**entity** | **Entity** |  (enum: posts, accounts, inbox, insights, ads, campaigns, ad-accounts) | 
**path** | **String** |  | 
**required_scope** | **Vec<String>** |  | 
**max_scope_ids** | **std::collections::HashMap<String, i32>** |  | 
**max_range_days** | **i32** |  | 
**default_range_days** | Option<**i32**> |  | 
**granularities** | **Vec<Granularities>** |  (enum: total, day, week, month) | 
**sorts** | **Vec<String>** |  | 
**max_sorted_rows** | Option<**i32**> |  | 
**includes** | [**Vec<models::MetricEntityIncludesInner>**](MetricEntityIncludesInner.md) |  | 
**group_by** | [**Vec<models::MetricEntityGroupByInner>**](MetricEntityGroupByInner.md) |  | 
**attributions** | [**Vec<models::MetricEntityAttributionsInner>**](MetricEntityAttributionsInner.md) |  | 
**origins** | **Vec<String>** |  | 
**metrics** | [**Vec<models::MetricDefinition>**](MetricDefinition.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


