# \TrackingLinksApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_tracking_link**](TrackingLinksApi.md#create_tracking_link) | **POST** /v1/tracking-links | Create a tracking link
[**delete_tracking_link**](TrackingLinksApi.md#delete_tracking_link) | **DELETE** /v1/tracking-links/{linkId} | Delete a tracking link
[**get_tracking_link**](TrackingLinksApi.md#get_tracking_link) | **GET** /v1/tracking-links/{linkId} | Get a tracking link
[**list_tracking_links**](TrackingLinksApi.md#list_tracking_links) | **GET** /v1/tracking-links | List tracking links
[**rotate_tracking_link_postback_token**](TrackingLinksApi.md#rotate_tracking_link_postback_token) | **POST** /v1/tracking-links/{linkId}/rotate-postback-token | Rotate a tracking link's postback URL
[**update_tracking_link**](TrackingLinksApi.md#update_tracking_link) | **PATCH** /v1/tracking-links/{linkId} | Update a tracking link



## create_tracking_link

> models::CreateTrackingLink201Response create_tracking_link(idempotency_key, create_tracking_link_request)
Create a tracking link

Creates a short link on a tracking site. Each click goes to one of `destinations`, picked by weight, so the link also split-tests landing pages. Put `url` in your ads and give `postbackUrl` to the network that reports conversions server to server. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**idempotency_key** | **String** | A unique key per link you create, such as a UUID. A retry with the same key and body returns the same link. | [required] |
**create_tracking_link_request** | [**CreateTrackingLinkRequest**](CreateTrackingLinkRequest.md) |  | [required] |

### Return type

[**models::CreateTrackingLink201Response**](createTrackingLink_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_tracking_link

> delete_tracking_link(link_id)
Delete a tracking link

The link and its postback URL stop working at once. Conversions already stored are kept.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**link_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_tracking_link

> models::CreateTrackingLink201Response get_tracking_link(link_id)
Get a tracking link

One link, with its URL and postback URL.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**link_id** | **String** |  | [required] |

### Return type

[**models::CreateTrackingLink201Response**](createTrackingLink_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_tracking_links

> models::ListTrackingLinks200Response list_tracking_links(profile_id, site_id, limit, cursor)
List tracking links

The tracking links of your workspace in creation order. Pass `profileId` or `siteId` to list one profile's or one site's links.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> |  |  |
**site_id** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**cursor** | Option<**String**> | `pagination.nextCursor` from the previous page. |  |

### Return type

[**models::ListTrackingLinks200Response**](listTrackingLinks_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## rotate_tracking_link_postback_token

> models::CreateTrackingLink201Response rotate_tracking_link_postback_token(link_id, idempotency_key)
Rotate a tracking link's postback URL

Issues a new `postbackUrl`. The old one stops working at once, so update it at the network right after.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**link_id** | **String** |  | [required] |
**idempotency_key** | **String** | A unique key per rotation, such as a UUID. | [required] |

### Return type

[**models::CreateTrackingLink201Response**](createTrackingLink_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_tracking_link

> models::CreateTrackingLink201Response update_tracking_link(link_id, update_tracking_link_request)
Update a tracking link

Changes the link's name, destinations, campaign hints or status. Send at least one field. `status: paused` turns the link off until it is set back to `active`. `campaign: null` removes the hints. The code and URL never change. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**link_id** | **String** |  | [required] |
**update_tracking_link_request** | [**UpdateTrackingLinkRequest**](UpdateTrackingLinkRequest.md) |  | [required] |

### Return type

[**models::CreateTrackingLink201Response**](createTrackingLink_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

