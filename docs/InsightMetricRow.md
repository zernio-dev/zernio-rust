# InsightMetricRow

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**date** | Option<**String**> | The day with granularity=day; fromDate with granularity=total; null for a lifetime total. With groupBy=demographic, the day the breakdown describes (meta.toDate). With groupBy=keyword, the first day of the months reported (meta.fromDate). | 
**breakdown** | Option<**String**> | With groupBy: the segment kind, such as age, country, hour or keyword; on Search Console, the dimensions grouped, such as query,country. | 
**dimension** | Option<**String**> | With groupBy: the segment value, such as 25-34, US, the hour 0 to 23 as Instagram reports it, or the search keyword. Search Console: the value when one dimension is grouped, null otherwise (see dimensions). | 
**dimension_id** | Option<**String**> | With groupBy=demographic on LinkedIn: the platform id of the segment. | 
**dimensions** | Option<**std::collections::HashMap<String, String>**> | Search Console with groupBy: the value of each dimension, such as { query, country }. country is an ISO 3166-1 alpha-3 code in lowercase; device is DESKTOP, MOBILE or TABLET. | [optional]
**metrics** | **std::collections::HashMap<String, f64>** | Each metric asked; null when the platform did not report it for the period. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


