# \TrackingTagsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_tracking_tag_shared_account**](TrackingTagsApi.md#add_tracking_tag_shared_account) | **POST** /v1/accounts/{accountId}/tracking-tags/{tagId}/shared-accounts | Share a tracking tag with an ad account
[**create_tracking_tag**](TrackingTagsApi.md#create_tracking_tag) | **POST** /v1/accounts/{accountId}/tracking-tags | Create a tracking tag (Meta Pixel)
[**get_tracking_tag**](TrackingTagsApi.md#get_tracking_tag) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId} | Fetch a single tracking tag (Meta Pixel)
[**get_tracking_tag_stats**](TrackingTagsApi.md#get_tracking_tag_stats) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/stats | Aggregated event stats for a tracking tag (Meta Pixel)
[**list_tracking_tag_shared_accounts**](TrackingTagsApi.md#list_tracking_tag_shared_accounts) | **GET** /v1/accounts/{accountId}/tracking-tags/{tagId}/shared-accounts | List ad accounts a tracking tag is shared with
[**list_tracking_tags**](TrackingTagsApi.md#list_tracking_tags) | **GET** /v1/accounts/{accountId}/tracking-tags | List tracking tags (Meta Pixels)
[**remove_tracking_tag_shared_account**](TrackingTagsApi.md#remove_tracking_tag_shared_account) | **DELETE** /v1/accounts/{accountId}/tracking-tags/{tagId}/shared-accounts | Stop sharing a tracking tag with an ad account
[**update_tracking_tag**](TrackingTagsApi.md#update_tracking_tag) | **PATCH** /v1/accounts/{accountId}/tracking-tags/{tagId} | Update a tracking tag (Meta Pixel)



## add_tracking_tag_shared_account

> models::AddTrackingTagSharedAccount201Response add_tracking_tag_shared_account(account_id, tag_id, add_tracking_tag_shared_account_request)
Share a tracking tag with an ad account

Shares the pixel with another ad account so campaigns/audiences in that account can use it. Requires that you administer both the pixel's owning Business Manager and the target ad account; a pixel on a personal (non-BM) ad account can't be shared (Meta will reject the call). Meta only (platform `metaads`); other platforms return 405. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** | Pixel id. | [required] |
**add_tracking_tag_shared_account_request** | [**AddTrackingTagSharedAccountRequest**](AddTrackingTagSharedAccountRequest.md) |  | [required] |

### Return type

[**models::AddTrackingTagSharedAccount201Response**](addTrackingTagSharedAccount_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_tracking_tag

> models::CreateTrackingTag201Response create_tracking_tag(account_id, create_tracking_tag_request)
Create a tracking tag (Meta Pixel)

Creates a Meta Pixel on the given ad account (`POST /act_{id}/adspixels` — `name` is the only input). Returns the created tag including its install `code`. The pixel is owned by the Business Manager that owns the ad account; a pixel created on a personal (non-BM) ad account ends up with `ownerBusinessId: null` and can't be shared with other ad accounts.  Creating a pixel does NOT install it — install the returned `code` snippet on the site, or send events server-side via `POST /v1/ads/conversions`. The check `installed` is derived from `lastFiredTime`.  NOT idempotent: each call creates a new pixel. Do not retry blindly on timeout. Meta only (platform `metaads`); other platforms return 405. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Meta ads SocialAccount id (platform `metaads`). | [required] |
**create_tracking_tag_request** | [**CreateTrackingTagRequest**](CreateTrackingTagRequest.md) |  | [required] |

### Return type

[**models::CreateTrackingTag201Response**](createTrackingTag_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_tracking_tag

> models::CreateTrackingTag201Response get_tracking_tag(account_id, tag_id)
Fetch a single tracking tag (Meta Pixel)

Returns the full tag record including the base-code `code` snippet, `lastFiredTime`, `ownerBusinessId`, `isUnavailable`, etc. Meta only (platform `metaads`); other platforms return 405. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** | Pixel id. | [required] |

### Return type

[**models::CreateTrackingTag201Response**](createTrackingTag_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_tracking_tag_stats

> models::GetTrackingTagStats200Response get_tracking_tag_stats(account_id, tag_id, aggregation, start_time, end_time)
Aggregated event stats for a tracking tag (Meta Pixel)

Returns aggregated event counts for the pixel (`GET /{pixel_id}/stats`). Rows are passed through from Meta as-is — their shape depends on the `aggregation` requested. Meta only (platform `metaads`); other platforms return 405. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** | Pixel id. | [required] |
**aggregation** | Option<**String**> | Aggregation dimension. Defaults to `event`. |  |[default to event]
**start_time** | Option<**i32**> | Unix seconds lower bound. |  |
**end_time** | Option<**i32**> | Unix seconds upper bound. |  |

### Return type

[**models::GetTrackingTagStats200Response**](getTrackingTagStats_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_tracking_tag_shared_accounts

> models::ListTrackingTagSharedAccounts200Response list_tracking_tag_shared_accounts(account_id, tag_id)
List ad accounts a tracking tag is shared with

Meta only (platform `metaads`); other platforms return 405.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** | Pixel id. | [required] |

### Return type

[**models::ListTrackingTagSharedAccounts200Response**](listTrackingTagSharedAccounts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_tracking_tags

> models::ListTrackingTags200Response list_tracking_tags(account_id, ad_account_id)
List tracking tags (Meta Pixels)

Returns the tracking tags (Meta Pixels) the connected ads account can see. Pass `?adAccountId=act_...` to scope the list to a single ad account; omit it to list every pixel reachable by the token (the name is then suffixed with the ad account it was discovered on, for disambiguation). The list view omits `code` — call `getTrackingTag` for the install snippet and full detail.  Meta only today (platform `metaads`); other platforms return 405. The `accountId` must be the Meta *ads* SocialAccount created by the Ads add-on connect flow, not a Facebook/Instagram posting account. Get your `act_...` ids from `GET /v1/ads/accounts`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Meta ads SocialAccount id (platform `metaads`). | [required] |
**ad_account_id** | Option<**String**> | Optional. Scope to one ad account, e.g. `act_123456789`. |  |

### Return type

[**models::ListTrackingTags200Response**](listTrackingTags_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_tracking_tag_shared_account

> remove_tracking_tag_shared_account(account_id, tag_id, ad_account_id)
Stop sharing a tracking tag with an ad account

`adAccountId` may be passed as a query parameter (recommended) or as a JSON body field for clients that can send DELETE bodies. Meta only (platform `metaads`); other platforms return 405. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** | Pixel id. | [required] |
**ad_account_id** | Option<**String**> | Ad account to unshare, e.g. `act_123456789`. May also be sent in the JSON body. |  |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_tracking_tag

> models::CreateTrackingTag201Response update_tracking_tag(account_id, tag_id, update_tracking_tag_request)
Update a tracking tag (Meta Pixel)

Partial-update a pixel. Whitelisted fields: `name` (rename), `enableAutomaticMatching`, `automaticMatchingFields`, `firstPartyCookieStatus`, `dataUseSetting`. At least one is required. Returns the re-fetched canonical tag. Meta only (platform `metaads`); other platforms return 405.  There is no DELETE — Meta has no API to delete a pixel. To stop using one, unshare it from your ad accounts (`DELETE .../tracking-tags/{tagId}/shared-accounts`) or disable it in Events Manager. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**tag_id** | **String** | Pixel id. | [required] |
**update_tracking_tag_request** | [**UpdateTrackingTagRequest**](UpdateTrackingTagRequest.md) |  | [required] |

### Return type

[**models::CreateTrackingTag201Response**](createTrackingTag_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

