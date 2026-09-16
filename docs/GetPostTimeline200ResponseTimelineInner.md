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
**follows** | Option<**i32**> | Follows attributed to the post on this date (Instagram feed and stories, TikTok business lane); 0 elsewhere | [optional]
**completion_rate** | Option<**f64**> | TikTok business lane: share of viewers who watched to the end on this date, 0 to 1; 0 elsewhere | [optional]
**profile_views** | Option<**i32**> | TikTok business lane: profile views attributed to the post on this date; 0 elsewhere | [optional]
**website_clicks** | Option<**i32**> | TikTok business lane: website-link clicks attributed to the post on this date (also inside clicks); 0 elsewhere | [optional]
**impression_sources** | Option<**std::collections::HashMap<String, f64>**> | TikTok business lane: share of views by surface on this date (forYou, follow, search, personalProfile, sound, directMessage, other), fractions 0 to 1; empty object elsewhere | [optional]
**audience_types** | Option<**std::collections::HashMap<String, f64>**> | TikTok business lane: follower / nonFollower and newViewer / returnViewer shares on this date, fractions 0 to 1; empty object elsewhere | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


