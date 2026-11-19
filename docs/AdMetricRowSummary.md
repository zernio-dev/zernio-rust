# AdMetricRowSummary

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**spend** | **f64** |  | 
**impressions** | **f64** |  | 
**reach** | **f64** | Deduplicated across days for Meta ads when the platform returns it. | 
**clicks** | **f64** |  | 
**engagement** | **f64** |  | 
**ctr** | **f64** |  | 
**cpc** | **f64** |  | 
**cpm** | **f64** |  | 
**conversions** | **f64** |  | 
**all_conversions** | **f64** |  | 
**cost_per_conversion** | **f64** |  | 
**actions** | **std::collections::HashMap<String, f64>** |  | 
**action_values** | **std::collections::HashMap<String, f64>** |  | 
**purchase_value** | **f64** |  | 
**roas** | **f64** |  | 
**cost_per_action** | **std::collections::HashMap<String, f64>** |  | 
**outbound_clicks** | **f64** |  | 
**outbound_clicks_ctr** | **f64** |  | 
**inline_link_clicks** | **f64** |  | 
**inline_link_click_ctr** | **f64** |  | 
**unique_clicks** | **f64** |  | 
**unique_ctr** | **f64** |  | 
**funnel** | **std::collections::HashMap<String, f64>** |  | 
**engagement_breakdown** | **std::collections::HashMap<String, f64>** |  | 
**video_play_actions** | **f64** |  | 
**video30_sec_watched_actions** | **f64** |  | 
**video_thruplay_watched_actions** | **f64** |  | 
**video_p25_watched_actions** | **f64** |  | 
**video_p50_watched_actions** | **f64** |  | 
**video_p75_watched_actions** | **f64** |  | 
**video_p95_watched_actions** | **f64** |  | 
**video_p100_watched_actions** | **f64** |  | 
**video_avg_time_watched_actions** | **f64** |  | 
**video2_sec_watched_actions** | **f64** |  | 
**video6_sec_watched_actions** | **f64** |  | 
**video6_sec_focused_views** | **f64** |  | 
**cost_per_thruplay** | **f64** |  | 
**last_synced_at** | Option<**String**> |  | 
**quality_ranking** | Option<**String**> |  | [optional]
**engagement_rate_ranking** | Option<**String**> |  | [optional]
**conversion_rate_ranking** | Option<**String**> |  | [optional]
**video_total_watch_time** | Option<**f64**> | Reading one ad: average watch time times plays, summed over the days. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


