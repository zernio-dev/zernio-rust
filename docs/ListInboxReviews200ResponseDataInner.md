# ListInboxReviews200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**account_username** | Option<**String**> |  | [optional]
**reviewer** | Option<[**models::ListInboxReviews200ResponseDataInnerReviewer**](ListInboxReviews200ResponseDataInnerReviewer.md)> |  | [optional]
**rating** | Option<**i32**> |  | [optional]
**text** | Option<**String**> |  | [optional]
**created** | Option<**String**> |  | [optional]
**has_reply** | Option<**bool**> |  | [optional]
**has_photos** | Option<**bool**> | Whether the review has at least one photo. Google Business only; always false for other platforms. | [optional]
**photo_count** | Option<**i32**> | Number of photos attached to the review (photos only; videos are not counted). Google Business only; 0 for other platforms. | [optional]
**photos** | Option<[**Vec<models::GetGoogleBusinessReviews200ResponseReviewsInnerPhotosInner>**](GetGoogleBusinessReviews200ResponseReviewsInnerPhotosInner.md)> | Photos attached to the review. Google Business only; always an empty array for other platforms. | [optional]
**reply** | Option<[**models::ListInboxReviews200ResponseDataInnerReply**](ListInboxReviews200ResponseDataInnerReply.md)> |  | [optional]
**review_url** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


