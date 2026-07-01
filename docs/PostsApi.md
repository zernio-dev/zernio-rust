# \PostsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bulk_upload_posts**](PostsApi.md#bulk_upload_posts) | **POST** /v1/posts/bulk-upload | Bulk upload from CSV
[**create_post**](PostsApi.md#create_post) | **POST** /v1/posts | Create post
[**delete_post**](PostsApi.md#delete_post) | **DELETE** /v1/posts/{postId} | Delete post
[**edit_post**](PostsApi.md#edit_post) | **POST** /v1/posts/{postId}/edit | Edit published post
[**get_post**](PostsApi.md#get_post) | **GET** /v1/posts/{postId} | Get post
[**list_posts**](PostsApi.md#list_posts) | **GET** /v1/posts | List posts
[**retry_post**](PostsApi.md#retry_post) | **POST** /v1/posts/{postId}/retry | Retry failed post
[**sync_external_posts**](PostsApi.md#sync_external_posts) | **POST** /v1/posts/sync-external | Sync or verify an external post on demand
[**unpublish_post**](PostsApi.md#unpublish_post) | **POST** /v1/posts/{postId}/unpublish | Unpublish post
[**update_post**](PostsApi.md#update_post) | **PUT** /v1/posts/{postId} | Update post
[**update_post_metadata**](PostsApi.md#update_post_metadata) | **POST** /v1/posts/{postId}/update-metadata | Update post metadata



## bulk_upload_posts

> models::BulkUploadResult bulk_upload_posts(dry_run, file)
Bulk upload from CSV

Create multiple posts by uploading a CSV file. Use dryRun=true to validate without creating posts.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dry_run** | Option<**bool**> |  |  |[default to false]
**file** | Option<**std::path::PathBuf**> |  |  |

### Return type

[**models::BulkUploadResult**](BulkUploadResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_post

> models::PostCreateResponse create_post(create_post_request, x_request_id)
Create post

Create and optionally publish a post. Immediate posts (`publishNow: true`) include `platformPostUrl` in the response. Content is optional when media is attached or all platforms have `customContent`. See each platform's schema for media constraints.  ## Idempotency  Two layers of duplicate-protection apply, so safe-to-retry callers (network blips, n8n / Zapier retries, etc.) don't accidentally double-post.  **1. Same-request idempotency (5-minute window).** Pass an `x-request-id` header to mark a logical request. If a second request arrives with the same `x-request-id` while the first is in-flight (or within ~5 minutes of completion), we return **HTTP 200** with the original post in the `existingPost` field — no new post is created. The official Zernio SDKs auto-generate a unique `x-request-id` per call. If you're using a generic HTTP client (curl, n8n's HTTP node, Zapier, custom code), either: - Set a unique `x-request-id` per logical call (recommended — UUIDv4 is fine) - Or simply omit the header — we'll treat each request as new  **Common pitfall**: if your workflow tool uses a single execution-level request ID and reuses it across multiple HTTP nodes (e.g. one ID for the whole run, shared across 6 different platform calls), every call after the first will look like a retry of the first and return its post. Generate a fresh ID per node.  **2. Content-hash dedup (24-hour window).** Independently, we hash `(platform, accountId, content + media URLs)` and reject duplicates within 24 hours with **HTTP 409**. This catches genuine \"same content posted twice to the same account\" cases regardless of `x-request-id`. Returns `error`, `accountId`, `platform`, and `existingPostId` so you can find the original. To intentionally re-post identical content within 24h, change something (the caption, the media, the account) — the dedup is keyed on the full content fingerprint.  Order: same-`x-request-id` retries (200) are checked first; if no idempotency match, the content-hash dedup (409) runs. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_post_request** | [**CreatePostRequest**](CreatePostRequest.md) |  | [required] |
**x_request_id** | Option<**uuid::Uuid**> | Optional client-generated request identifier for safe retry (idempotency). When two requests carry the same value, the second is treated as a retry of the first and returns the original post (HTTP 200) instead of creating a duplicate. Window is ~5 minutes from the first request. Generate a UUID per logical call. SDKs do this automatically; HTTP clients should set it themselves or omit it. See the operation description for the full idempotency contract.  |  |

### Return type

[**models::PostCreateResponse**](PostCreateResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_post

> models::PostDeleteResponse delete_post(post_id)
Delete post

Delete a draft or scheduled post from Zernio. Published posts cannot be deleted; use the Unpublish endpoint instead. Upload quota is automatically refunded.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |

### Return type

[**models::PostDeleteResponse**](PostDeleteResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## edit_post

> models::EditPost200Response edit_post(post_id, edit_post_request)
Edit published post

Edit a published post on a social media platform. Currently only supported for X (Twitter).  Requirements: - Connected X account must have an active X Premium subscription - Must be within 1 hour of original publish time - Maximum 5 edits per tweet (enforced by X) - Text-only edits (media changes are not supported)  The post record in Zernio is updated with the new content and edit history. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |
**edit_post_request** | [**EditPostRequest**](EditPostRequest.md) |  | [required] |

### Return type

[**models::EditPost200Response**](editPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_post

> models::PostGetResponse get_post(post_id)
Get post

Fetch a single post by ID. For published posts, this returns platformPostUrl for each platform. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |

### Return type

[**models::PostGetResponse**](PostGetResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_posts

> models::PostsListResponse list_posts(page, limit, source, status, platform, profile_id, created_by, date_from, date_to, include_hidden, search, sort_by, account_id)
List posts

Returns a paginated list of posts. Published posts include platformPostUrl with the public URL on each platform.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page** | Option<**i32**> | Page number (1-based) |  |[default to 1]
**limit** | Option<**i32**> | Page size |  |[default to 10]
**source** | Option<**String**> | Which collection to read. `zernio` (default) returns posts authored through Zernio. `external` returns posts synced from the platform (existing/historical posts that were published outside Zernio). Combine with `accountId` and paginate via `page`/`limit` to walk the full synced history (we keep up to the last ~12 months per account). |  |[default to zernio]
**status** | Option<**String**> |  |  |
**platform** | Option<**String**> |  |  |
**profile_id** | Option<**String**> |  |  |
**created_by** | Option<**String**> |  |  |
**date_from** | Option<**String**> |  |  |
**date_to** | Option<**String**> |  |  |
**include_hidden** | Option<**bool**> |  |  |[default to false]
**search** | Option<**String**> | Search posts by text content. |  |
**sort_by** | Option<**String**> | Sort order for results. |  |[default to scheduled-desc]
**account_id** | Option<**String**> | Filter posts to those published via a specific social account (24-char hex ObjectId). |  |

### Return type

[**models::PostsListResponse**](PostsListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## retry_post

> models::PostRetryResponse retry_post(post_id)
Retry failed post

Immediately retries publishing a failed post. Returns the updated post with its new status.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |

### Return type

[**models::PostRetryResponse**](PostRetryResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## sync_external_posts

> models::SyncExternalPosts200Response sync_external_posts(sync_external_posts_request)
Sync or verify an external post on demand

Fetch an account's latest external posts (published directly on the platform, not through Zernio) on demand, so a just-published post is retrievable within seconds instead of waiting for the background sync (which refreshes each account at most every ~90 minutes).  Primary use case: verifying a submitted post. When a user publishes on the platform and immediately pastes the post URL into your app, call this with `accountId` plus `url` (or `postId`) to confirm the post exists and return its metadata.  Behavior: - We check our stored copy first and return immediately if the post is already known (no platform call). - Otherwise we fetch the account's latest posts live from the platform, then match and return the submitted post. - Requests are debounced per account (~15s): if the account was just synced, the live fetch is skipped.  `accountId` is required — a post URL or id alone cannot be resolved to an account, and the account must be connected to Zernio (we use its token to read the platform). Supported for every platform with a listing API (Instagram, Facebook, TikTok, YouTube, X, Threads, Pinterest, Reddit, Bluesky, Google Business, and LinkedIn organization accounts; LinkedIn personal accounts are not supported).  `url` accepts any format the platform uses (e.g. `instagram.com/p/…`, `instagram.com/reel/…`, `youtu.be/…`, `youtube.com/shorts/…`, `tiktok.com/@user/video/…`, and `vm.tiktok.com` short links). Pass `postId` (the platform media/video id) as an alternative locator.  Note: post-level analytics (reach, impressions) still carry the platform's own delay (e.g. ~24h on Instagram). This endpoint confirms the post exists and returns its metadata plus basic engagement (likes, comments), not delayed insights. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sync_external_posts_request** | [**SyncExternalPostsRequest**](SyncExternalPostsRequest.md) |  | [required] |

### Return type

[**models::SyncExternalPosts200Response**](syncExternalPosts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## unpublish_post

> models::UnpublishPost200Response unpublish_post(post_id, unpublish_post_request)
Unpublish post

Deletes a published post from the specified platform. The post record in Zernio is kept but its status is updated to cancelled. Not supported on Instagram, TikTok, or Snapchat. Threaded posts delete all items. YouTube deletion is permanent. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |
**unpublish_post_request** | [**UnpublishPostRequest**](UnpublishPostRequest.md) |  | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_post

> models::PostUpdateResponse update_post(post_id, update_post_request)
Update post

Update an existing post. Draft, scheduled, failed, partial, and cancelled posts can be edited. Published posts can only have their recycling config updated. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** |  | [required] |
**update_post_request** | [**UpdatePostRequest**](UpdatePostRequest.md) |  | [required] |

### Return type

[**models::PostUpdateResponse**](PostUpdateResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_post_metadata

> models::UpdatePostMetadata200Response update_post_metadata(post_id, update_post_metadata_request)
Update post metadata

Updates metadata of a published video on the specified platform without re-uploading. Currently only supported for YouTube. At least one updatable field is required.  Two modes:  1. Post-based (video published through Zernio): pass the Zernio postId in the URL and platform in the body. 2. Direct video ID (video uploaded outside Zernio, e.g. directly to YouTube): use _ as the postId,    and pass videoId + accountId + platform in the body. The accountId is the Zernio social account ID    for the connected YouTube channel. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**post_id** | **String** | Zernio post ID, or \"_\" when using direct video ID mode | [required] |
**update_post_metadata_request** | [**UpdatePostMetadataRequest**](UpdatePostMetadataRequest.md) |  | [required] |

### Return type

[**models::UpdatePostMetadata200Response**](updatePostMetadata_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

