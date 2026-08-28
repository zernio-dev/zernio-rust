# \ReviewsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_inbox_review_reply**](ReviewsApi.md#delete_inbox_review_reply) | **DELETE** /v1/inbox/reviews/{reviewId}/reply | Delete review reply
[**list_inbox_reviews**](ReviewsApi.md#list_inbox_reviews) | **GET** /v1/inbox/reviews | List reviews
[**reply_to_inbox_review**](ReviewsApi.md#reply_to_inbox_review) | **POST** /v1/inbox/reviews/{reviewId}/reply | Reply to review



## delete_inbox_review_reply

> models::DeleteInboxReviewReply200Response delete_inbox_review_reply(review_id, delete_inbox_review_reply_request)
Delete review reply

Delete a reply to a review (Google Business only). Requires accountId in request body.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**review_id** | **String** |  | [required] |
**delete_inbox_review_reply_request** | [**DeleteInboxReviewReplyRequest**](DeleteInboxReviewReplyRequest.md) |  | [required] |

### Return type

[**models::DeleteInboxReviewReply200Response**](deleteInboxReviewReply_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_inbox_reviews

> models::ListInboxReviews200Response list_inbox_reviews(profile_id, platform, min_rating, max_rating, has_reply, sort_by, sort_order, limit, cursor, account_id)
List reviews

Fetch reviews from all connected Facebook Pages and Google Business accounts. Aggregates data with filtering and sorting options. Supported platforms: Facebook, Google Business. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> |  |  |
**platform** | Option<**String**> |  |  |
**min_rating** | Option<**i32**> |  |  |
**max_rating** | Option<**i32**> |  |  |
**has_reply** | Option<**bool**> | Filter by reply status |  |
**sort_by** | Option<**String**> |  |  |[default to date]
**sort_order** | Option<**String**> |  |  |[default to desc]
**limit** | Option<**i32**> |  |  |[default to 25]
**cursor** | Option<**String**> |  |  |
**account_id** | Option<**String**> | Filter by specific social account ID |  |

### Return type

[**models::ListInboxReviews200Response**](listInboxReviews_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reply_to_inbox_review

> models::ReplyToInboxReview200Response reply_to_inbox_review(review_id, reply_to_inbox_review_request, idempotency_key)
Reply to review

Post a reply to a review. Requires accountId in request body.  **Idempotency:** send an `Idempotency-Key` header to make retries safe (e.g. after a client-side timeout where delivery is unknown): same key + same body replays the original response (with `Idempotent-Replayed: true`) instead of sending the reply to the platform again; same key + different body returns 422; a key still in flight returns 409. Keys are retained for 24 hours and are scoped to the credential and to this exact path, so reusing a key against a different reviewId returns 422 rather than replaying the other review's response.  Only successful (2xx) responses are stored for replay. If the request throws or returns a non-2xx status the key is released, so the header protects the \"request succeeded but the response was lost\" case. After an ambiguous failure (a 5xx or a network timeout) fetch the review before retrying with the same key, and treat a missing reply as inconclusive rather than as proof nothing was sent. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**review_id** | **String** | Review ID (URL-encoded for Google Business) | [required] |
**reply_to_inbox_review_request** | [**ReplyToInboxReviewRequest**](ReplyToInboxReviewRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. |  |

### Return type

[**models::ReplyToInboxReview200Response**](replyToInboxReview_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

