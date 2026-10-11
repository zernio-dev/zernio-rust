# GetPostTimeline200ResponseTimelineInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**date** | Option<[**String**](String.md)> | Date in YYYY-MM-DD format | [optional]
**platform** | Option<**String**> | Platform name (e.g. instagram, tiktok) | [optional]
**platform_post_id** | Option<**String**> | Platform-specific post ID | [optional]
**impressions** | Option<**i32**> | Total impressions on this date | [optional]
**reach** | Option<**i32**> | Total reach on this date | [optional]
**likes** | Option<**i32**> | Total likes on this date | [optional]
**comments** | Option<**i32**> | Total comments on this date | [optional]
**shares** | Option<**i32**> | Total shares on this date | [optional]
**saves** | Option<**i32**> | Total saves on this date | [optional]
**clicks** | Option<**i32**> | Total clicks on this date | [optional]
**views** | Option<**i32**> | Total views on this date | [optional]
**follows** | Option<**i32**> | Follows attributed to the post on this date (Instagram feed and stories, Facebook Reels, TikTok business lane). Null on Instagram Reels and video and on Facebook posts that are not Reels, where Meta has no follows metric; 0 on other platforms. | [optional]
**completion_rate** | Option<**f64**> | TikTok business lane: share of viewers who watched to the end on this date, 0 to 1; 0 elsewhere | [optional]
**profile_views** | Option<**i32**> | TikTok business lane: profile views attributed to the post on this date; 0 elsewhere | [optional]
**website_clicks** | Option<**i32**> | TikTok business lane: website-link clicks attributed to the post on this date (also inside clicks); 0 elsewhere | [optional]
**impression_sources** | Option<**std::collections::HashMap<String, f64>**> | TikTok business lane: share of views by surface on this date (forYou, follow, search, personalProfile, sound, directMessage, other), fractions 0 to 1; empty object elsewhere | [optional]
**audience_types** | Option<**std::collections::HashMap<String, f64>**> | TikTok business lane: follower / nonFollower and newViewer / returnViewer shares on this date, fractions 0 to 1; empty object elsewhere | [optional]
**audience_countries** | Option<**std::collections::HashMap<String, f64>**> | TikTok business lane: viewer-country shares on this date keyed by ISO-3166 alpha-2, fractions 0 to 1, top 20 with the tail in `other`; empty object elsewhere | [optional]
**replays** | Option<**i32**> | Facebook Reels only: plays that were replays, as of this date; 0 elsewhere | [optional]
**retention_curve** | Option<**std::collections::HashMap<String, f64>**> | Facebook Reels and TikTok business lane: share still watching at each second of playback, fractions 0 to 1. Facebook Reels (Meta post_video_retention_graph): the base is a subset of plays that Meta selects and does not expose: on small Reels it can be far below views (6 of 51 measured), so a value is a share of that subset, not of all plays. Keys are whole seconds from the start of a play (\"3\" is the share still watching at 3 s). Loops count as continued playback, so a short Reels curve runs past its length (an 8 s Reel has keys \"0\" to \"12\"); Meta returns at most 41 points, so a long Reel covers only its first 40 s. TikTok accounts connected through the TikTok for Business app also fill it from TikTok video_view_retention: share still watching at each whole second, fractions 0 to 1, at most 61 points, thinned evenly on videos longer than 60 s. Values are as of this date; empty object for other media and platforms. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


