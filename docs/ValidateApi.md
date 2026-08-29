# \ValidateApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**validate_media**](ValidateApi.md#validate_media) | **POST** /v1/tools/validate/media | Validate media URL
[**validate_post**](ValidateApi.md#validate_post) | **POST** /v1/tools/validate/post | Validate post content
[**validate_post_length**](ValidateApi.md#validate_post_length) | **POST** /v1/tools/validate/post-length | Validate character count
[**validate_subreddit**](ValidateApi.md#validate_subreddit) | **GET** /v1/tools/validate/subreddit | Check subreddit existence



## validate_media

> models::ValidateMedia200Response validate_media(validate_media_request)
Validate media URL

Check if a media URL is accessible and return metadata (content type, file size) plus per-platform size limit comparisons.  Performs a HEAD request (with GET fallback) to detect content type and size. Rejects private/localhost URLs for SSRF protection.  Platform limits are sourced from each platform's actual upload constraints. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**validate_media_request** | [**ValidateMediaRequest**](ValidateMediaRequest.md) |  | [required] |

### Return type

[**models::ValidateMedia200Response**](validateMedia_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## validate_post

> models::ValidatePost200Response validate_post(validate_post_request)
Validate post content

Dry-run the full post validation pipeline without publishing. Catches issues like missing media for Instagram/TikTok/YouTube, hashtag limits, invalid thread formats, Facebook Reel requirements, and character limit violations.  Accepts the same body as POST /v1/posts. Does NOT validate accounts, process media, or track usage. Account lookups are limit-only: a twitter accountId is resolved, scoped to the caller, only to pick the 280 vs 25000 character limit. Missing, foreign, or invalid ids fall back to 280 and never error.  Returns errors for failures and warnings for near-limit content (>90% of character limit). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**validate_post_request** | [**ValidatePostRequest**](ValidatePostRequest.md) |  | [required] |

### Return type

[**models::ValidatePost200Response**](validatePost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## validate_post_length

> models::ValidatePostLength200Response validate_post_length(validate_post_length_request)
Validate character count

Check weighted character count per platform and whether the text is within each platform's limit.  Twitter/X uses weighted counting (URLs = 23 chars via t.co, emojis = 2 chars). All other platforms use plain character length.  Returns counts and limits for all 15 supported platform variants.  X (Twitter) returns two rows and this endpoint cannot tell you which one applies to you: it takes only `text`, so it never resolves an account. `twitter` (280) is the free tier limit. `twitterPremium` (25000) applies only when the target X account has a paid X subscription, and publishing enforces 280 instead for any post carrying a poll (this endpoint has no poll input, so the `twitterPremium` row always shows 25000). A free account trusting the `twitterPremium` row can pass validation here and still fail at publish time, where the account's real limit is enforced.  To validate against the per-account limit, use `POST /v1/tools/validate/post` instead: it accepts an `accountId` per platform entry, resolves X Premium status, and checks the text against the limit publishing enforces, including the poll cap. A missing, foreign, or invalid `accountId` falls back to the conservative 280. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**validate_post_length_request** | [**ValidatePostLengthRequest**](ValidatePostLengthRequest.md) |  | [required] |

### Return type

[**models::ValidatePostLength200Response**](validatePostLength_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## validate_subreddit

> models::ValidateSubreddit200Response validate_subreddit(name, account_id)
Check subreddit existence

Check if a subreddit exists and return basic info (title, subscriber count, NSFW status, post types allowed).  When accountId is provided, uses authenticated Reddit OAuth API with automatic token refresh (recommended). Falls back to Reddit's public JSON API, which may be unreliable from server IPs. Returns exists: false for private, banned, or nonexistent subreddits. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**name** | **String** | Subreddit name (with or without \"r/\" prefix) | [required] |
**account_id** | Option<**String**> | Reddit social account ID for authenticated lookup (recommended for reliable results) |  |

### Return type

[**models::ValidateSubreddit200Response**](validateSubreddit_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

