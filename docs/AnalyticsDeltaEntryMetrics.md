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
**follows** | **i32** | Follows attributed to this post (Instagram feed and stories, Facebook Reels, TikTok business lane) | 
**ig_reels_avg_watch_time** | **i32** | Average watch time per play, in milliseconds (Instagram Reels, Facebook Reels, TikTok business videos) | 
**ig_reels_video_view_total_time** | **i32** | Total watch time including replays, in milliseconds (Instagram Reels, Facebook Reels, TikTok business videos) | 
**reposts** | **i32** |  | 
**reels_skip_rate** | **f64** | Instagram Reels skip rate, 0 to 1 | 
**completion_rate** | **f64** | TikTok business lane: share of viewers who watched to the end, 0 to 1 | 
**profile_views** | **i32** | TikTok business lane: profile views attributed to the post | 
**website_clicks** | **i32** | TikTok business lane: website-link clicks attributed to the post (also inside clicks) | 
**impression_sources** | **std::collections::HashMap<String, f64>** | TikTok business lane: share of views by surface (forYou, follow, search, personalProfile, sound, directMessage, other), fractions 0 to 1. Empty object elsewhere. | 
**audience_types** | **std::collections::HashMap<String, f64>** | TikTok business lane: follower / nonFollower and newViewer / returnViewer shares, fractions 0 to 1. Empty object elsewhere. | 
**audience_countries** | **std::collections::HashMap<String, f64>** | TikTok business lane: viewer-country shares keyed by ISO-3166 alpha-2, fractions 0 to 1, top 20 with the tail in `other`. Empty object elsewhere. | 
**replays** | Option<**i32**> | Facebook Reels only: plays that were replays. 0 elsewhere. | [optional]
**retention_curve** | Option<**std::collections::HashMap<String, f64>**> | Facebook Reels only: share still watching at each second of playback, fractions 0 to 1 (Meta post_video_retention_graph). The base is a subset of plays that Meta selects and does not expose: on small Reels it can be far below views (6 of 51 measured), so a value is a share of that subset, not of all plays. Keys are whole seconds from the start of a play (\"3\" is the share still watching at 3 s). Loops count as continued playback, so a short Reels curve runs past its length (an 8 s Reel has keys \"0\" to \"12\"); Meta returns at most 41 points, so a long Reel covers only its first 40 s. Empty object elsewhere. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


