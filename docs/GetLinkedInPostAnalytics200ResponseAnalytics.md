# GetLinkedInPostAnalytics200ResponseAnalytics

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**impressions** | Option<**i32**> | Times the post was shown | [optional]
**reach** | Option<**i32**> | Unique members who saw the post | [optional]
**likes** | Option<**i32**> | Reactions on the post | [optional]
**comments** | Option<**i32**> | Comments on the post | [optional]
**shares** | Option<**i32**> | Reshares of the post | [optional]
**saves** | Option<**i32**> | Times the post was saved (personal accounts only; 0 for organization accounts) | [optional]
**sends** | Option<**i32**> | Times the post was sent via LinkedIn messaging (personal accounts only; 0 for organization accounts) | [optional]
**clicks** | Option<**i32**> | Clicks on the post (organization accounts only) | [optional]
**views** | Option<**i32**> | Video views (video posts only) | [optional]
**engagement_rate** | Option<**f64**> | Engagement rate, as a percentage rounded to 2 decimals: (likes + comments + shares + clicks + saves + sends) / impressions * 100. Unlike PostAnalytics.engagementRate on GET /v1/analytics, this one DOES count clicks and has no fallback denominator, so it is 0 whenever impressions is 0. For organization accounts the value is the rate LinkedIn returns, not one computed here. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


