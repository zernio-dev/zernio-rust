# PostAnalytics

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**impressions** | Option<**i32**> |  | [optional]
**reach** | Option<**i32**> |  | [optional]
**likes** | Option<**i32**> |  | [optional]
**comments** | Option<**i32**> |  | [optional]
**shares** | Option<**i32**> |  | [optional]
**saves** | Option<**i32**> | Number of saves/bookmarks (Instagram, Pinterest, X/Twitter) | [optional]
**clicks** | Option<**i32**> |  | [optional]
**views** | Option<**i32**> |  | [optional]
**follows** | Option<**i32**> | Instagram feed posts and stories only: organic accounts that started following from this post. Null on Instagram Reels and non-Reels video, where Meta does not expose this metric for the media. 0 for other platforms. | [optional]
**ig_reels_avg_watch_time** | Option<**i32**> | Instagram Reels only: average watch time per play, in milliseconds. 0 for non-Reels media and other platforms. | [optional]
**ig_reels_video_view_total_time** | Option<**i32**> | Instagram Reels only: total watch time including replays, in milliseconds. 0 for non-Reels media and other platforms. | [optional]
**reels_skip_rate** | Option<**f64**> | Instagram Reels only: the rate of initial views that skipped the reel within its first 3 seconds, as reported by Meta. Passed through exactly as Meta reports it, with no rescaling, so do not assume a 0-1 share. Meta labels the metric estimated and in development, so it can move between syncs. 0 for non-Reels media and other platforms. When a post is published to several accounts, the aggregate is weighted by views. | [optional]
**reposts** | Option<**i32**> | Instagram only: reposts of the media by other users, minus deleted reposts. Available on feed posts, reels and stories. 0 for other platforms, including Threads, where reposts are counted in shares instead. | [optional]
**video_duration_seconds** | Option<**i32**> | Video length in seconds. Currently Instagram Reels only; combine with igReelsAvgWatchTime (ms) to estimate retention. Null when unknown (other platforms, non-video media, or when Instagram does not expose the media URL, e.g. reels with copyrighted audio). | [optional]
**engagement_rate** | Option<**f64**> | Percentage, rounded to 2 decimals: (likes + comments + shares + saves) / (impressions or reach or views) * 100. Clicks and follows are never counted. The denominator is the FIRST of impressions, reach, views that is non-zero, so it is not the same basis on every post: a post with impressions divides by impressions, one without falls back to reach, then to views. If you need a single consistent basis (e.g. interactions / reach), compute it from the raw fields above. The engagementRate on the LinkedIn account endpoints is a different formula. | [optional]
**last_updated** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


