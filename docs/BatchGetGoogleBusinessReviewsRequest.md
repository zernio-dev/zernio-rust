# BatchGetGoogleBusinessReviewsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**location_names** | **Vec<String>** | Array of full location resource names (e.g. ['accounts/123/locations/456']). Max 50 per request (Google's batchGetReviews cap); chunk larger sets into multiple requests. | 
**page_size** | Option<**i32**> | Number of reviews per page (max 50) | [optional][default to 50]
**page_token** | Option<**String**> | Pagination token from previous response | [optional]
**order_by** | Option<**OrderBy**> | Sort order requested from Google. Defaults to 'updateTime desc' (newest first), which allows early-stopping pagination once results cross your date window. (enum: updateTime desc, rating, rating desc) | [optional][default to UpdateTimeDesc]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


