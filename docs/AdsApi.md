# \AdsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**boost_post**](AdsApi.md#boost_post) | **POST** /v1/ads/boost | Boost an existing post as a paid ad
[**create_standalone_ad**](AdsApi.md#create_standalone_ad) | **POST** /v1/ads/create | Create a standalone ad with custom creative
[**delete_ad**](AdsApi.md#delete_ad) | **DELETE** /v1/ads/{adId} | Cancel an ad
[**get_ad**](AdsApi.md#get_ad) | **GET** /v1/ads/{adId} | Get ad details
[**get_ad_analytics**](AdsApi.md#get_ad_analytics) | **GET** /v1/ads/{adId}/analytics | Get ad analytics with daily breakdown
[**list_ad_accounts**](AdsApi.md#list_ad_accounts) | **GET** /v1/ads/accounts | List ad accounts for a social account
[**list_ads**](AdsApi.md#list_ads) | **GET** /v1/ads | List ads
[**search_ad_interests**](AdsApi.md#search_ad_interests) | **GET** /v1/ads/interests | Search targeting interests
[**update_ad**](AdsApi.md#update_ad) | **PUT** /v1/ads/{adId} | Update ad (pause/resume, budget, targeting, name)



## boost_post

> models::UpdateAd200Response boost_post(boost_post_request)
Boost an existing post as a paid ad

Creates a paid ad campaign from an existing published post. Creates the full platform campaign hierarchy (campaign, ad set, ad).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**boost_post_request** | [**BoostPostRequest**](BoostPostRequest.md) |  | [required] |

### Return type

[**models::UpdateAd200Response**](updateAd_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_standalone_ad

> models::UpdateAd200Response create_standalone_ad(create_standalone_ad_request)
Create a standalone ad with custom creative

Creates a paid ad with custom creative (headline, body, image/video, link). Creates the full platform campaign hierarchy.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_standalone_ad_request** | [**CreateStandaloneAdRequest**](CreateStandaloneAdRequest.md) |  | [required] |

### Return type

[**models::UpdateAd200Response**](updateAd_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_ad

> models::DeleteAccountGroup200Response delete_ad(ad_id)
Cancel an ad

Cancels the ad on the platform and marks it as cancelled in the database. The ad is preserved for history.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** |  | [required] |

### Return type

[**models::DeleteAccountGroup200Response**](deleteAccountGroup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad

> models::GetAd200Response get_ad(ad_id)
Get ad details

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** |  | [required] |

### Return type

[**models::GetAd200Response**](getAd_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_analytics

> models::GetAdAnalytics200Response get_ad_analytics(ad_id, from_date, to_date, breakdowns)
Get ad analytics with daily breakdown

Returns detailed performance analytics for an ad. Includes summary metrics, a daily timeline over the requested date range, and optional demographic breakdowns (Meta and TikTok only). If no date range is provided, defaults to the last 90 days. Date range is capped at 90 days max. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** |  | [required] |
**from_date** | Option<**String**> | Start of date range (YYYY-MM-DD). Defaults to 90 days ago. |  |
**to_date** | Option<**String**> | End of date range (YYYY-MM-DD). Defaults to today. Max 90-day range. |  |
**breakdowns** | Option<**String**> | Comma-separated breakdown dimensions. Meta: age, gender, country, publisher_platform, device_platform, region. TikTok: gender, age, country_code, platform, ac, language. |  |

### Return type

[**models::GetAdAnalytics200Response**](getAdAnalytics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_accounts

> models::ListAdAccounts200Response list_ad_accounts(account_id)
List ad accounts for a social account

Returns the platform ad accounts available for the given social account (e.g. Meta ad accounts, TikTok advertiser IDs, Google Ads customer IDs).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Social account ID | [required] |

### Return type

[**models::ListAdAccounts200Response**](listAdAccounts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ads

> models::ListAds200Response list_ads(page, limit, source, status, platform, account_id, ad_account_id, profile_id, campaign_id, from_date, to_date)
List ads

Returns a paginated list of ads with metrics computed over an optional date range. Use `source=all` to include externally-synced ads from platform ad managers. If no date range is provided, defaults to the last 90 days. Date range is capped at 90 days max. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page** | Option<**i32**> | Page number (1-based) |  |[default to 1]
**limit** | Option<**i32**> |  |  |[default to 50]
**source** | Option<**String**> | zernio = Zernio-created only, all = include external ads |  |[default to zernio]
**status** | Option<**String**> |  |  |
**platform** | Option<**String**> |  |  |
**account_id** | Option<**String**> | Social account ID |  |
**ad_account_id** | Option<**String**> | Platform ad account ID (e.g. act_123 for Meta). Mirrors the same filter on /v1/ads/campaigns and /v1/ads/tree. |  |
**profile_id** | Option<**String**> | Profile ID |  |
**campaign_id** | Option<**String**> | Platform campaign ID (filter ads within a campaign) |  |
**from_date** | Option<**String**> | Start of metrics date range (YYYY-MM-DD). Defaults to 90 days ago. |  |
**to_date** | Option<**String**> | End of metrics date range (YYYY-MM-DD). Defaults to today. Max 90-day range. |  |

### Return type

[**models::ListAds200Response**](listAds_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_ad_interests

> models::SearchAdInterests200Response search_ad_interests(q, account_id)
Search targeting interests

Search for interest-based targeting options available on the platform.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**q** | **String** | Search query | [required] |
**account_id** | **String** | Social account ID | [required] |

### Return type

[**models::SearchAdInterests200Response**](searchAdInterests_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad

> models::UpdateAd200Response update_ad(ad_id, update_ad_request)
Update ad (pause/resume, budget, targeting, name)

Update one or more fields on an ad. Status changes and budget updates are propagated to the platform. Targeting updates are Meta-only.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** |  | [required] |
**update_ad_request** | [**UpdateAdRequest**](UpdateAdRequest.md) |  | [required] |

### Return type

[**models::UpdateAd200Response**](updateAd_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

