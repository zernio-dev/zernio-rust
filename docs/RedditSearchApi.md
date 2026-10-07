# \RedditSearchApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_reddit_feed**](RedditSearchApi.md#get_reddit_feed) | **GET** /v1/reddit/feed | Get subreddit feed
[**get_reddit_post_comments**](RedditSearchApi.md#get_reddit_post_comments) | **GET** /v1/reddit/comments/{postId} | Get the comments of a Reddit post
[**search_reddit**](RedditSearchApi.md#search_reddit) | **GET** /v1/reddit/search | Search posts



## get_reddit_feed

> models::SearchReddit200Response get_reddit_feed(account_id, subreddit, sort, limit, after, t)
Get subreddit feed

Fetch posts from a subreddit feed. Supports sorting, time filtering, and cursor-based pagination.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**subreddit** | Option<**String**> |  |  |
**sort** | Option<**String**> |  |  |[default to hot]
**limit** | Option<**i32**> |  |  |[default to 25]
**after** | Option<**String**> |  |  |
**t** | Option<**String**> |  |  |

### Return type

[**models::SearchReddit200Response**](searchReddit_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_reddit_post_comments

> models::GetRedditPostComments200Response get_reddit_post_comments(post_id, account_id, sort, limit, comment_id)
Get the comments of a Reddit post

Reads the comments of any Reddit post the connected account can see, for example one found through `/v1/reddit/feed` or `/v1/reddit/search`, straight from Reddit on every call. The tree comes flattened in thread order (a reply follows its parent); rebuild it from `parentId`, which is `t3_…` for a reply to the post and `t1_…` for a reply to a comment. Deleted and removed comments are passed through as Reddit sends them (`[deleted]` / `[removed]`). Where Reddit truncates a thread, the ids it left out are listed in `more`; `commentId` fetches one such comment with its replies. A post Reddit no longer serves answers 404 and a private subreddit 403, both with `platform_api_error`. For comments on posts published through Zernio, `/v1/inbox/comments/{postId}` adds caching, moderation and replies. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | Reddit post id, with or without the `t3_` prefix (as `id` or `fullname` on RedditPost). | [required] |
**account_id** | **String** | An active Reddit account the request is made as. | [required] |
**sort** | Option<**String**> |  |  |[default to new]
**limit** | Option<**i32**> | Maximum number of top-level comments. |  |[default to 25]
**comment_id** | Option<**String**> | Return only this comment and its replies, with or without the `t1_` prefix; pass an id from `more` to expand it. |  |

### Return type

[**models::GetRedditPostComments200Response**](getRedditPostComments_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_reddit

> models::SearchReddit200Response search_reddit(account_id, q, subreddit, restrict_sr, sort, limit, after)
Search posts

Search Reddit posts using a connected account. Optionally scope to a specific subreddit.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**q** | **String** |  | [required] |
**subreddit** | Option<**String**> |  |  |
**restrict_sr** | Option<**String**> |  |  |
**sort** | Option<**String**> |  |  |[default to new]
**limit** | Option<**i32**> |  |  |[default to 25]
**after** | Option<**String**> |  |  |

### Return type

[**models::SearchReddit200Response**](searchReddit_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

