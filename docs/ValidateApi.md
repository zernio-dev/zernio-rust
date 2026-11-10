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

Check that a media URL is reachable and that its bytes are a real image, video or PDF, then return metadata (detected format, file size, dimensions) plus per-platform size limit comparisons.  `valid: true` means the content was verified, not just the extension or Content-Type:  - Images up to 32 MB are fully decoded (`inspection: decoded`). - Videos, PDFs and larger images are verified by their file signature and header (`inspection: header`). - The type and format come from the bytes, not the Content-Type header. - Corrupt, truncated or non-media files return `valid: false` with code `MEDIA_UNDECODABLE`. - Private/localhost URLs are rejected for SSRF protection. - A Google Drive share link is checked against the file behind it. A file not shared as \"Anyone with the link\" returns `valid: false` with code `MEDIA_URL_UNREACHABLE`.  Platform limits are sourced from each platform's actual upload constraints. 

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

Dry-run the full post validation pipeline without publishing. Catches issues like missing media for Instagram/TikTok/YouTube, hashtag limits, invalid thread formats, Facebook Reel requirements, and character limit violations.  Accepts the same body as POST /v1/posts. Does NOT validate accounts, transform media, or track usage. Account lookups are limit-only: a twitter accountId is resolved, scoped to the caller, only to pick the 280 vs 25000 character limit. Missing, foreign, or invalid ids fall back to 280 and never error.  Every image, gif and video URL in `mediaItems` and `customMedia` is fetched and checked:  - A file that is not a real image, video or PDF (wrong bytes, truncated, corrupt) is an error with code `MEDIA_UNDECODABLE`. - Images are checked at header level. The full file is decoded only when the header is not enough. Use POST /v1/tools/validate/media for a full pixel decode. - A URL our servers cannot fetch is a warning, not an error, because the platform may still reach it.  Returns errors for failures and warnings for near-limit content (>90% of character limit). 

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

Check weighted character count per platform and whether the text is within each platform's limit.  Returns counts and limits for all 15 supported platform variants.  ### Counting  - X uses weighted counting (URLs = 23 chars via t.co, emojis = 2 chars). - All other platforms use plain character length.  ### X rows  X returns two rows, and this endpoint cannot tell you which one applies to you: it takes only `text`, so it never resolves an account.  - `twitter` (280) is the free tier limit. - `twitterPremium` (25000) applies only when the target X account has a paid X subscription. Publishing enforces 280 instead for any post carrying a poll. This endpoint has no poll input, so the `twitterPremium` row always shows 25000.  A free account trusting the `twitterPremium` row can pass validation here and still fail at publish time, where the account's real limit is enforced.  ### Per-account limits  To validate against the per-account limit, use `POST /v1/tools/validate/post` instead. It accepts an `accountId` per platform entry, resolves X Premium status, and checks the text against the limit publishing enforces, including the poll cap.  A missing, foreign, or invalid `accountId` falls back to the conservative 280. 

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

Temporarily unavailable: Reddit has blocked third-party apps from its API, so this endpoint returns 503 `PLATFORM_DISABLED` until Reddit restores access. Reddit Ads is not affected.  Check if a subreddit exists and return basic info (title, subscriber count, NSFW status, post types allowed).  When accountId is provided, uses authenticated Reddit OAuth API with automatic token refresh (recommended). Falls back to Reddit's public JSON API, which may be unreliable from server IPs. Returns exists: false for private, banned, or nonexistent subreddits. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**name** | **String** | Subreddit name (with or without \"r/\" prefix) | [required] |
**account_id** | Option<**String**> | Reddit account ID for authenticated lookup (recommended for reliable results) |  |

### Return type

[**models::ValidateSubreddit200Response**](validateSubreddit_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

