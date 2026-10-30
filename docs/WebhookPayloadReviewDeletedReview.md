# WebhookPayloadReviewDeletedReview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Full review name, matching review.id on the review.new event (\"accounts/123/locations/456/reviews/789\"). | 
**platform** | **Platform** |  (enum: googlebusiness) | 
**rating** | Option<**i32**> | Star rating the reviewer gave. Null when it was never recorded. | 
**created_at** | Option<**String**> | When the reviewer posted the review. Null when it was never recorded. | 
**last_seen_at** | **String** | Last time Zernio saw Google return this review. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


