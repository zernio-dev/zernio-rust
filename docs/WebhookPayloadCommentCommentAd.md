# WebhookPayloadCommentCommentAd

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Meta ad ID (Instagram only). | [optional]
**title** | Option<**String**> | Ad creative title (Instagram only). | [optional]
**original_media_id** | Option<**String**> | Original media ID that Meta reports for the ad (Instagram only). | [optional]
**promotion_status** | Option<**String**> | Facebook only. The parent post's promotion_status as the Graph API returns it, for example \"active\" (organic post currently boosted). Ad dark posts usually report \"inactive\" and sometimes \"ineligible\", so use isDarkPost, not this value, to tell an ad comment apart.  | [optional]
**is_dark_post** | Option<**bool**> | Facebook only: true when the post is an unpublished ad creative (dark post), false for a boosted organic post. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


