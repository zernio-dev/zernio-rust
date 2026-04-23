# ReviewWebhookReview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Platform review ID (e.g. \"accounts/123/locations/456/reviews/789\" for Google Business). | 
**platform** | **Platform** | Platform the review originated on. Currently Google Business Profile only. (enum: googlebusiness) | 
**rating** | **i32** | Star rating the reviewer gave. | 
**text** | **String** | Review text content. May be empty if the reviewer left only a rating. | 
**reviewer** | [**models::ReviewWebhookReviewReviewer**](ReviewWebhookReviewReviewer.md) |  | 
**created_at** | **String** |  | 
**has_reply** | **bool** | Whether the connected account has replied to this review. | 
**reply** | Option<[**models::ReviewWebhookReviewReply**](ReviewWebhookReviewReply.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


