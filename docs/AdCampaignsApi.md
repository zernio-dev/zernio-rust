# \AdCampaignsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_ad_tree**](AdCampaignsApi.md#get_ad_tree) | **GET** /v1/ads/tree | Get campaign tree
[**list_ad_campaigns**](AdCampaignsApi.md#list_ad_campaigns) | **GET** /v1/ads/campaigns | List campaigns
[**update_ad_campaign_status**](AdCampaignsApi.md#update_ad_campaign_status) | **PUT** /v1/ads/campaigns/{campaignId}/status | Pause or resume a campaign



## get_ad_tree

> models::GetAdTree200Response get_ad_tree(page, limit, source, platform, status, ad_account_id, account_id, profile_id, from_date, to_date)
Get campaign tree

Returns a nested Campaign > Ad Set > Ad hierarchy with rolled-up metrics at each level. Uses a two-stage aggregation: ads are grouped into ad sets, then ad sets into campaigns. Metrics are computed over an optional date range, then rolled up from ad level to ad set and campaign levels. Pagination is at the campaign level. Ads without a campaign or ad set ID are grouped into synthetic \"Ungrouped\" buckets. If no date range is provided, defaults to the last 90 days. Date range is capped at 90 days max. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page** | Option<**i32**> | Page number (1-based) |  |[default to 1]
**limit** | Option<**i32**> | Campaigns per page |  |[default to 20]
**source** | Option<**String**> |  |  |[default to zernio]
**platform** | Option<**String**> |  |  |
**status** | Option<[**AdStatus**](AdStatus.md)> | Filter by derived campaign status (post-aggregation) |  |
**ad_account_id** | Option<**String**> | Platform ad account ID |  |
**account_id** | Option<**String**> | Social account ID |  |
**profile_id** | Option<**String**> | Profile ID |  |
**from_date** | Option<**String**> | Start of metrics date range (YYYY-MM-DD). Defaults to 90 days ago. |  |
**to_date** | Option<**String**> | End of metrics date range (YYYY-MM-DD). Defaults to today. Max 90-day range. |  |

### Return type

[**models::GetAdTree200Response**](getAdTree_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_campaigns

> models::ListAdCampaigns200Response list_ad_campaigns(page, limit, source, platform, status, ad_account_id, account_id, profile_id)
List campaigns

Returns campaigns as virtual aggregations over ad documents grouped by platform campaign ID. Metrics (spend, impressions, clicks, etc.) are summed across all ads in each campaign. Campaign status is derived from child ad statuses (active > pending_review > paused > error > completed > cancelled > rejected). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page** | Option<**i32**> | Page number (1-based) |  |[default to 1]
**limit** | Option<**i32**> |  |  |[default to 20]
**source** | Option<**String**> |  |  |[default to zernio]
**platform** | Option<**String**> |  |  |
**status** | Option<[**AdStatus**](AdStatus.md)> | Filter by derived campaign status (post-aggregation) |  |
**ad_account_id** | Option<**String**> | Platform ad account ID (e.g. act_123 for Meta) |  |
**account_id** | Option<**String**> | Social account ID |  |
**profile_id** | Option<**String**> | Profile ID |  |

### Return type

[**models::ListAdCampaigns200Response**](listAdCampaigns_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad_campaign_status

> models::UpdateAdCampaignStatus200Response update_ad_campaign_status(campaign_id, update_ad_campaign_status_request)
Pause or resume a campaign

Updates the status of all ads in a campaign. Makes one platform API call (not per-ad) since status cascades through the campaign hierarchy. Ads in terminal statuses (rejected, completed, cancelled) are automatically skipped. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Platform campaign ID | [required] |
**update_ad_campaign_status_request** | [**UpdateAdCampaignStatusRequest**](UpdateAdCampaignStatusRequest.md) |  | [required] |

### Return type

[**models::UpdateAdCampaignStatus200Response**](updateAdCampaignStatus_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

