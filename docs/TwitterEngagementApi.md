# \TwitterEngagementApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bookmark_post**](TwitterEngagementApi.md#bookmark_post) | **POST** /v1/twitter/bookmark | Bookmark a tweet
[**follow_user**](TwitterEngagementApi.md#follow_user) | **POST** /v1/twitter/follow | Follow a user
[**get_tweet**](TwitterEngagementApi.md#get_tweet) | **GET** /v1/twitter/tweet | Look up a tweet
[**remove_bookmark**](TwitterEngagementApi.md#remove_bookmark) | **DELETE** /v1/twitter/bookmark | Remove bookmark
[**retweet_post**](TwitterEngagementApi.md#retweet_post) | **POST** /v1/twitter/retweet | Retweet a post
[**search_tweets**](TwitterEngagementApi.md#search_tweets) | **GET** /v1/twitter/search | Search recent tweets
[**undo_retweet**](TwitterEngagementApi.md#undo_retweet) | **DELETE** /v1/twitter/retweet | Undo retweet
[**unfollow_user**](TwitterEngagementApi.md#unfollow_user) | **DELETE** /v1/twitter/follow | Unfollow a user



## bookmark_post

> models::BookmarkPost200Response bookmark_post(bookmark_post_request)
Bookmark a tweet

Bookmark a tweet by ID. Requires the bookmark.write OAuth scope. Rate limit: 50 requests per 15-min window. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**bookmark_post_request** | [**BookmarkPostRequest**](BookmarkPostRequest.md) |  | [required] |

### Return type

[**models::BookmarkPost200Response**](bookmarkPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## follow_user

> models::FollowUser200Response follow_user(follow_user_request)
Follow a user

Follow a user on X/Twitter. Requires the follows.write OAuth scope. For protected accounts, a follow request is sent instead (pending_follow will be true). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**follow_user_request** | [**FollowUserRequest**](FollowUserRequest.md) |  | [required] |

### Return type

[**models::FollowUser200Response**](followUser_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_tweet

> models::GetTweet200Response get_tweet(account_id, id)
Look up a tweet

Resolve a single tweet by ID or URL into its text, author and public metrics.  Use this to render a post you are referencing, e.g. the tweet quoted by a quote-style post. Unlike `/v1/twitter/search` this is not limited to the last 7 days and works for any tweet visible to the connected account.  Billed as an X posts read ($0.005). Repeat lookups of the same tweet within the same UTC day are charged once. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The social account ID whose X token is used for the lookup | [required] |
**id** | **String** | Numeric tweet ID or a tweet URL (e.g. https://x.com/user/status/123...) | [required] |

### Return type

[**models::GetTweet200Response**](getTweet_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_bookmark

> models::RemoveBookmark200Response remove_bookmark(account_id, tweet_id)
Remove bookmark

Remove a bookmark from a tweet. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tweet_id** | **String** | The ID of the tweet to unbookmark | [required] |

### Return type

[**models::RemoveBookmark200Response**](removeBookmark_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## retweet_post

> models::RetweetPost200Response retweet_post(retweet_post_request)
Retweet a post

Retweet (repost) a tweet by ID. Rate limit: 50 requests per 15-min window. Shares the 300/3hr creation limit with tweet creation. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**retweet_post_request** | [**RetweetPostRequest**](RetweetPostRequest.md) |  | [required] |

### Return type

[**models::RetweetPost200Response**](retweetPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_tweets

> models::SearchTweets200Response search_tweets(account_id, query, limit, since_id, until_id, start_time, end_time, cursor, sort_order)
Search recent tweets

Search public tweets from the last 7 days matching an X search query, e.g. to discover tweets to reply to. The query string is passed through to X unchanged and supports X's search operators (`from:user`, `-is:retweet`, `is:reply`, `lang:en`, `\"exact phrase\"`, `conversation_id:123`, boolean `OR`, ...). Note that standalone operators like `is:` / `has:` / `lang:` must be combined with a keyword or `from:` clause.  To reply to a found tweet, pass its `id` as the twitter platform entry's `platformSpecificData.replyToTweetId` when creating a post.  Rate limit: 300 requests per 15-min window per connected account. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The social account ID | [required] |
**query** | **String** | X search query, max 512 characters. Operators are passed through unchanged; X rejects malformed queries with a 400. | [required] |
**limit** | Option<**i32**> | Results per page. X requires a minimum of 10; values below 10 are rejected. |  |[default to 10]
**since_id** | Option<**String**> | Only return tweets with an ID greater than (more recent than) this numeric tweet ID. Non-numeric values are rejected with 400. |  |
**until_id** | Option<**String**> | Only return tweets with an ID less than (older than) this numeric tweet ID. Non-numeric values are rejected with 400. |  |
**start_time** | Option<**String**> | Oldest UTC timestamp (ISO 8601, inclusive), within the last 7 days |  |
**end_time** | Option<**String**> | Newest UTC timestamp (ISO 8601, exclusive), within the last 7 days |  |
**cursor** | Option<**String**> | Pagination cursor from a previous response |  |
**sort_order** | Option<**String**> |  |  |[default to recency]

### Return type

[**models::SearchTweets200Response**](searchTweets_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## undo_retweet

> models::UndoRetweet200Response undo_retweet(account_id, tweet_id)
Undo retweet

Undo a retweet (un-repost a tweet). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tweet_id** | **String** | The ID of the original tweet to un-retweet | [required] |

### Return type

[**models::UndoRetweet200Response**](undoRetweet_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## unfollow_user

> models::UnfollowUser200Response unfollow_user(account_id, target_user_id)
Unfollow a user

Unfollow a user on X/Twitter. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**target_user_id** | **String** | The Twitter ID of the user to unfollow | [required] |

### Return type

[**models::UnfollowUser200Response**](unfollowUser_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

