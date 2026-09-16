# AnalyticsDeltaEntryMetrics

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**impressions** | **i32** |  | 
**reach** | **i32** |  | 
**likes** | **i32** |  | 
**comments** | **i32** |  | 
**shares** | **i32** |  | 
**saves** | **i32** |  | 
**sends** | **i32** |  | 
**clicks** | **i32** |  | 
**views** | **i32** |  | 
**follows** | **i32** | Follows attributed to this post (Instagram) | 
**ig_reels_avg_watch_time** | **i32** | Instagram Reels average watch time, in milliseconds | 
**ig_reels_video_view_total_time** | **i32** | Instagram Reels total watch time, in milliseconds | 
**reposts** | **i32** |  | 
**reels_skip_rate** | **f64** | Instagram Reels skip rate, 0 to 1 | 
**completion_rate** | **f64** | TikTok business lane: share of viewers who watched to the end, 0 to 1 | 
**profile_views** | **i32** | TikTok business lane: profile views attributed to the post | 
**website_clicks** | **i32** | TikTok business lane: website-link clicks attributed to the post (also inside clicks) | 
**impression_sources** | **std::collections::HashMap<String, f64>** | TikTok business lane: share of views by surface (forYou, follow, search, personalProfile, sound, directMessage, other), fractions 0 to 1. Empty object elsewhere. | 
**audience_types** | **std::collections::HashMap<String, f64>** | TikTok business lane: follower / nonFollower and newViewer / returnViewer shares, fractions 0 to 1. Empty object elsewhere. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


