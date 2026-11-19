# InsightMetricsResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**entity** | **Entity** |  (enum: insights) | 
**account_id** | **String** |  | 
**platform_post_id** | Option<**String**> |  | 
**platform** | **String** |  | 
**granularity** | **Granularity** |  (enum: total, day) | 
**group_by** | **String** | none, demographic, hour, keyword, or the Search Console dimensions grouped, such as query,country. | 
**timeframe** | Option<**Timeframe**> | Instagram demographics: the period Instagram aggregated. (enum: this_week, this_month, ) | 
**from_date** | Option<**String**> | Null for a lifetime or snapshot demographic breakdown. | 
**to_date** | Option<**String**> |  | 
**unavailable_metrics** | [**Vec<models::InsightMetricsResponseMetaUnavailableMetricsInner>**](InsightMetricsResponseMetaUnavailableMetricsInner.md) | Metrics asked that the platform could not answer for this account, with the reason. | 
**units** | [**std::collections::HashMap<String, models::InsightMetricsResponseMetaUnitsValue>**](InsightMetricsResponseMetaUnitsValue.md) | Monetary metrics: the unit and currency the platform reports them in. Demographic metrics: count, share (0 to 1) or percent (0 to 100). | 
**data_delay** | Option<**String**> | How late the platform reports these metrics, in words. Search Console: the rows cover final days only. | 
**provisional_since** | Option<**String**> | First day the platform may still revise or have missing. Post insights only; null on account insights and when every day is final. | 
**stale** | **bool** | True when the platform refused the refresh and the answer is the last stored copy. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


