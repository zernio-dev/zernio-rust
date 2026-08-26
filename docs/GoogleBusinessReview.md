# GoogleBusinessReview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Review ID | [optional]
**name** | Option<**String**> | Full resource name | [optional]
**reviewer** | Option<[**models::GoogleBusinessReviewReviewer**](GoogleBusinessReviewReviewer.md)> |  | [optional]
**rating** | Option<**i32**> | Numeric star rating (0 when Google sends no rating) | [optional]
**star_rating** | Option<**StarRating**> | Google's string rating (enum: ONE, TWO, THREE, FOUR, FIVE) | [optional]
**comment** | Option<**String**> | Review text | [optional]
**create_time** | Option<**String**> |  | [optional]
**update_time** | Option<**String**> |  | [optional]
**review_reply** | Option<[**models::GoogleBusinessReviewReviewReply**](GoogleBusinessReviewReviewReply.md)> |  | [optional]
**photo_count** | Option<**i32**> | Number of photos attached to the review (photos only, videos are not counted) | [optional]
**photos** | Option<[**Vec<models::ListInboxReviews200ResponseDataInnerPhotosInner>**](ListInboxReviews200ResponseDataInnerPhotosInner.md)> | Photos attached to the review by the reviewer | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


