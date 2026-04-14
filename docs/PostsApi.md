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
[**unpublish_post**](PostsApi.md#unpublish_post) | **POST** /v1/posts/{postId}/unpublish | Unpublish post
[**update_post**](PostsApi.md#update_post) | **PUT** /v1/posts/{postId} | Update post
[**update_post_metadata**](PostsApi.md#update_post_metadata) | **POST** /v1/posts/{postId}/update-metadata | Update post metadata



## bulk_upload_posts

> models::BulkUploadPosts200Response bulk_upload_posts(dry_run, file)
Bulk upload from CSV

Create multiple posts by uploading a CSV file. Use dryRun=true to validate without creating posts.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**dry_run** | Option<**bool**> |  |  |[default to false]
**file** | Option<**std::path::PathBuf**> |  |  |

### Return type

[**models::BulkUploadPosts200Response**](bulkUploadPosts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_post

> models::PostCreateResponse create_post(create_post_request)
Create post

Create and optionally publish a post. Immediate posts (publishNow: true) include platformPostUrl in the response. Content is optional when media is attached or all platforms have customContent. See each platform's schema for media constraints. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_post_request** | [**CreatePostRequest**](CreatePostRequest.md) |  | [required] |

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

> models::PostsListResponse list_posts(page, limit, status, platform, profile_id, created_by, date_from, date_to, include_hidden, search, sort_by)
List posts

Returns a paginated list of posts. Published posts include platformPostUrl with the public URL on each platform.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page** | Option<**i32**> | Page number (1-based) |  |[default to 1]
**limit** | Option<**i32**> | Page size |  |[default to 10]
**status** | Option<**String**> |  |  |
**platform** | Option<**String**> |  |  |
**profile_id** | Option<**String**> |  |  |
**created_by** | Option<**String**> |  |  |
**date_from** | Option<**String**> |  |  |
**date_to** | Option<**String**> |  |  |
**include_hidden** | Option<**bool**> |  |  |[default to false]
**search** | Option<**String**> | Search posts by text content. |  |
**sort_by** | Option<**String**> | Sort order for results. |  |[default to scheduled-desc]

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

Update an existing post. Only draft, scheduled, failed, and partial posts can be edited. Published, publishing, and cancelled posts cannot be modified. 

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

