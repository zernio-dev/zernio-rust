# AdEngagementCounts

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**post_engagement** | Option<**i32**> | Meta's own post-engagement total (`post_engagement`). | [optional]
**page_engagement** | Option<**i32**> | Meta's own page-engagement total (`page_engagement`). | [optional]
**reactions** | Option<**i32**> | Reactions on the ad's post (`post_reaction`). | [optional]
**comments** | Option<**i32**> | Comments on the ad's post. | [optional]
**shares** | Option<**i32**> | Shares of the ad's post. Meta reports these under the action type literally named `post`. | [optional]
**saves** | Option<**i32**> | Saves of the ad's post (`onsite_conversion.post_save`). | [optional]
**page_likes** | Option<**i32**> | New Page likes attributed to the ad (`like`). | [optional]
**video_views** | Option<**i32**> | 3-second video views (`video_view`). For completion-based counts use `videoThruplayWatchedActions`. | [optional]
**link_clicks** | Option<**i32**> | Attributed link clicks (`link_click`). This is the attribution-window count, which differs from the in-session count in the sibling `inlineLinkClicks` field. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


