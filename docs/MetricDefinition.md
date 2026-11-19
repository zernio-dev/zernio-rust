# MetricDefinition

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**description** | **String** |  | 
**unit** | **Unit** | ratio is a plain ratio (0 to 1 for a rate); money is in the account currency, or the unit and currency meta.units gives; position is a rank where 1 is the top; score runs from 0 to 100. (enum: count, milliseconds, percent, seconds, minutes, ratio, money, position, score) | 
**additive** | **bool** |  | 
**source** | **Source** | stored: read from what Zernio synced; live: read from the platform on each request. (enum: stored, live) | 
**platforms** | **Vec<String>** |  | 
**freshness** | **String** |  | 
**granularities** | **Vec<Granularities>** |  (enum: total, day, week, month) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


