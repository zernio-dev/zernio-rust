# \GmbReviewsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**batch_get_google_business_reviews**](GmbReviewsApi.md#batch_get_google_business_reviews) | **POST** /v1/accounts/{accountId}/gmb-reviews/batch | Batch get reviews
[**delete_google_business_review_reply**](GmbReviewsApi.md#delete_google_business_review_reply) | **DELETE** /v1/accounts/{accountId}/gmb-reviews/{reviewId}/reply | Delete a review reply
[**get_google_business_reviews**](GmbReviewsApi.md#get_google_business_reviews) | **GET** /v1/accounts/{accountId}/gmb-reviews | Get reviews
[**reply_to_google_business_review**](GmbReviewsApi.md#reply_to_google_business_review) | **POST** /v1/accounts/{accountId}/gmb-reviews/{reviewId}/reply | Reply to a review



## batch_get_google_business_reviews

> models::BatchGetGoogleBusinessReviews200Response batch_get_google_business_reviews(account_id, batch_get_google_business_reviews_request)
Batch get reviews

Fetches reviews across multiple locations in a single request. More efficient than calling GET /gmb-reviews per location for multi-location businesses. Returns a flat locationReviews array (not grouped by location): each item carries the location resource name it belongs to (`name`) plus the review object (`review`), whose identity is `review.reviewId`. Reviews are requested from Google ordered by `orderBy` (default `updateTime desc`, newest first), so callers polling for recent reviews can stop paginating once they cross their date window. Note: this endpoint does not return aggregate metrics (averageRating / totalReviewCount). For those, use the single-location GET /gmb-reviews endpoint. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**batch_get_google_business_reviews_request** | [**BatchGetGoogleBusinessReviewsRequest**](BatchGetGoogleBusinessReviewsRequest.md) |  | [required] |

### Return type

[**models::BatchGetGoogleBusinessReviews200Response**](batchGetGoogleBusinessReviews_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_google_business_review_reply

> models::DeleteGoogleBusinessReviewReply200Response delete_google_business_review_reply(account_id, review_id)
Delete a review reply

Removes the business owner reply from a Google Business review. The review itself remains.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio account ID (from /v1/accounts) | [required] |
**review_id** | **String** | The review ID portion (e.g. \"AIe9_BGx1234567890\"), not the full resource name | [required] |

### Return type

[**models::DeleteGoogleBusinessReviewReply200Response**](deleteGoogleBusinessReviewReply_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_google_business_reviews

> models::GetGoogleBusinessReviews200Response get_google_business_reviews(account_id, location_id, page_size, page_token)
Get reviews

Returns reviews for a GBP account including ratings, comments, and owner replies. Use nextPageToken for pagination.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio account ID (from /v1/accounts) | [required] |
**location_id** | Option<**String**> | Override which location to query. If omitted, uses the account's selected location. Use GET /gmb-locations to list valid IDs. |  |
**page_size** | Option<**i32**> | Number of reviews to fetch per page (max 50) |  |[default to 50]
**page_token** | Option<**String**> | Pagination token from previous response |  |

### Return type

[**models::GetGoogleBusinessReviews200Response**](getGoogleBusinessReviews_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reply_to_google_business_review

> models::ReplyToGoogleBusinessReview200Response reply_to_google_business_review(account_id, review_id, reply_to_google_business_review_request)
Reply to a review

Posts (or updates) the business owner reply to a Google Business review. The reply is associated with the account's currently selected location (set via /v1/accounts/{accountId}/gmb-locations). Calling this endpoint a second time on the same review overwrites the previous reply (PUT semantics on Google's side). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio account ID (from /v1/accounts) | [required] |
**review_id** | **String** | The review ID portion (e.g. \"AIe9_BGx1234567890\"), not the full resource name | [required] |
**reply_to_google_business_review_request** | [**ReplyToGoogleBusinessReviewRequest**](ReplyToGoogleBusinessReviewRequest.md) |  | [required] |

### Return type

[**models::ReplyToGoogleBusinessReview200Response**](replyToGoogleBusinessReview_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

