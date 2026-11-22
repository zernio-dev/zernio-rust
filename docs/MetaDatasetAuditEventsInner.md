# MetaDatasetAuditEventsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**last7_days** | **i32** |  | 
**last24_hours** | **i32** |  | 
**last_seen_hour** | Option<**String**> | Start of the last hour Meta counted the event in: Meta's stats are hourly. | 
**daily** | [**Vec<models::MetaDatasetAuditEventsInnerDailyInner>**](MetaDatasetAuditEventsInnerDailyInner.md) |  | 
**server_share_pct** | Option<**f64**> | Percent of the window's events received through the Conversions API. Null when not measured (only the 12 busiest events are split by source). | 
**match_quality** | Option<**f64**> | Event Match Quality, 0 to 10. Meta rates 6 and above as good. | 
**match_keys** | [**Vec<models::MetaDatasetAuditEventsInnerMatchKeysInner>**](MetaDatasetAuditEventsInnerMatchKeysInner.md) |  | 
**diagnostics** | [**Vec<models::MetaDatasetAuditEventsInnerDiagnosticsInner>**](MetaDatasetAuditEventsInnerDiagnosticsInner.md) |  | 
**dedup** | [**Vec<models::MetaDatasetAuditEventsInnerDedupInner>**](MetaDatasetAuditEventsInnerDedupInner.md) | Per deduplication key, the share of browser and server copies carrying it and of browser copies Meta paired through it. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


