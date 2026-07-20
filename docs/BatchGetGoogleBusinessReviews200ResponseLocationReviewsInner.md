# BatchGetGoogleBusinessReviews200ResponseLocationReviewsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> | LOCATION resource name the review belongs to (accounts/{accountId}/locations/{locationId}) - NOT the review resource name. Use it to attribute the review to a location; the review identity is review.reviewId (full review resource name at review.name). | [optional]
**review** | Option<**serde_json::Value**> | The review object: reviewId (the review's identity), name (full review resource name, accounts/_*_/locations/_*_/reviews/_*), starRating, comment, reviewer, createTime, updateTime, reviewReply, and reviewMediaItems (review photos/videos; photo items carry thumbnailUrl, video items carry videoUrl) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


