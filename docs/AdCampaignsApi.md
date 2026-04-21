# \AdCampaignsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bulk_update_ad_campaign_status**](AdCampaignsApi.md#bulk_update_ad_campaign_status) | **POST** /v1/ads/campaigns/bulk-status | Pause or resume many campaigns
[**delete_ad_campaign**](AdCampaignsApi.md#delete_ad_campaign) | **DELETE** /v1/ads/campaigns/{campaignId} | Delete a campaign
[**duplicate_ad_campaign**](AdCampaignsApi.md#duplicate_ad_campaign) | **POST** /v1/ads/campaigns/{campaignId}/duplicate | Duplicate a campaign
[**get_ad_tree**](AdCampaignsApi.md#get_ad_tree) | **GET** /v1/ads/tree | Get campaign tree
[**list_ad_campaigns**](AdCampaignsApi.md#list_ad_campaigns) | **GET** /v1/ads/campaigns | List campaigns
[**update_ad_campaign**](AdCampaignsApi.md#update_ad_campaign) | **PUT** /v1/ads/campaigns/{campaignId} | Update a campaign (budget)
[**update_ad_campaign_status**](AdCampaignsApi.md#update_ad_campaign_status) | **PUT** /v1/ads/campaigns/{campaignId}/status | Pause or resume a campaign
[**update_ad_set**](AdCampaignsApi.md#update_ad_set) | **PUT** /v1/ads/ad-sets/{adSetId} | Update an ad set (budget and/or status)
[**update_ad_set_status**](AdCampaignsApi.md#update_ad_set_status) | **PUT** /v1/ads/ad-sets/{adSetId}/status | Pause or resume a single ad set



## bulk_update_ad_campaign_status

> models::BulkUpdateAdCampaignStatus200Response bulk_update_ad_campaign_status(bulk_update_ad_campaign_status_request)
Pause or resume many campaigns

Process up to 50 campaigns in one call. Each campaign is updated concurrently and the response contains a per-campaign result so a single bad row does not fail the whole batch. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**bulk_update_ad_campaign_status_request** | [**BulkUpdateAdCampaignStatusRequest**](BulkUpdateAdCampaignStatusRequest.md) |  | [required] |

### Return type

[**models::BulkUpdateAdCampaignStatus200Response**](bulkUpdateAdCampaignStatus_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_ad_campaign

> models::DeleteAdCampaign200Response delete_ad_campaign(campaign_id, delete_ad_campaign_request)
Delete a campaign

Deletes the whole campaign on the platform, cascading to its ad sets and ads. Locally, all Ad documents for this campaign are marked `status: cancelled`.  Meta-only for now. Other platforms return 501 Not Implemented — fall back to DELETE /v1/ads/{adId} per ad in the meantime. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Platform campaign ID | [required] |
**delete_ad_campaign_request** | [**DeleteAdCampaignRequest**](DeleteAdCampaignRequest.md) |  | [required] |

### Return type

[**models::DeleteAdCampaign200Response**](deleteAdCampaign_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## duplicate_ad_campaign

> models::DuplicateAdCampaign200Response duplicate_ad_campaign(campaign_id, duplicate_ad_campaign_request)
Duplicate a campaign

Duplicates a campaign, including its ad sets, ads, creatives, and targeting by default (`deepCopy: true`). On Meta, this uses `POST /{campaign-id}/copies`. The copy is created paused by default so callers can review before launching.  The platform's duplication is asynchronous from our side; once the copy is created on the platform, we trigger a sync discovery so the new hierarchy shows up in /v1/ads/tree. Set `syncAfter: false` to skip the discovery trigger and poll on your own cadence.  Meta-only for now. Other platforms return 501 Not Implemented. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Source platform campaign ID | [required] |
**duplicate_ad_campaign_request** | [**DuplicateAdCampaignRequest**](DuplicateAdCampaignRequest.md) |  | [required] |

### Return type

[**models::DuplicateAdCampaign200Response**](duplicateAdCampaign_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_tree

> models::GetAdTree200Response get_ad_tree(page, limit, source, platform, status, ad_account_id, account_id, profile_id, from_date, to_date)
Get campaign tree

Returns a nested Campaign > Ad Set > Ad hierarchy with rolled-up metrics at each level. Uses a two-stage aggregation: ads are grouped into ad sets, then ad sets into campaigns. Metrics are computed over an optional date range, then rolled up from ad level to ad set and campaign levels. Pagination is at the campaign level. Ads without a campaign or ad set ID are grouped into synthetic \"Ungrouped\" buckets. If no date range is provided, defaults to the last 90 days. Date range is capped at 90 days max. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page** | Option<**i32**> | Page number (1-based) |  |[default to 1]
**limit** | Option<**i32**> | Campaigns per page |  |[default to 20]
**source** | Option<**String**> | `all` (default) returns both Zernio-created ads and those discovered from the platform's ad manager — matches the web UI's default view. Pass `zernio` to restrict to isExternal=false only. Status is NOT filtered by default — use the `status` param for that. |  |[default to all]
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
**source** | Option<**String**> | `all` (default) returns both Zernio-created ads and those discovered from the platform's ad manager — matches the web UI's default view. Pass `zernio` to restrict to isExternal=false only. Status is NOT filtered by default — use the `status` param for that. |  |[default to all]
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


## update_ad_campaign

> models::UpdateAdCampaign200Response update_ad_campaign(campaign_id, update_ad_campaign_request)
Update a campaign (budget)

Campaign-level edits. Currently supports updating the CBO (Campaign Budget Optimization) budget. For ABO campaigns (where the budget lives on the ad set), use PUT /v1/ads/ad-sets/{adSetId} instead — this endpoint will return 409 with code BUDGET_LEVEL_MISMATCH.  Meta-only for now. Other platforms return 501 Not Implemented. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Platform campaign ID | [required] |
**update_ad_campaign_request** | [**UpdateAdCampaignRequest**](UpdateAdCampaignRequest.md) |  | [required] |

### Return type

[**models::UpdateAdCampaign200Response**](updateAdCampaign_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
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


## update_ad_set

> models::UpdateAdSet200Response update_ad_set(ad_set_id, update_ad_set_request)
Update an ad set (budget and/or status)

Ad-set-level writes. Use this for ABO budget updates and ad-set-scoped pause/resume. Provide `budget` and/or `status` in the body.  When updating `budget` on an ABO campaign: if the parent campaign is CBO, the response is 409 with code BUDGET_LEVEL_MISMATCH — route to PUT /v1/ads/campaigns/{campaignId} instead. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_set_id** | **String** | Platform ad set ID | [required] |
**update_ad_set_request** | [**UpdateAdSetRequest**](UpdateAdSetRequest.md) |  | [required] |

### Return type

[**models::UpdateAdSet200Response**](updateAdSet_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad_set_status

> models::UpdateAdSetStatus200Response update_ad_set_status(ad_set_id, update_ad_campaign_status_request)
Pause or resume a single ad set

Ad-set-scoped pause/resume (doesn't touch sibling ad sets). Thin wrapper over PUT /v1/ads/ad-sets/{adSetId} for callers that only want the status toggle and prefer a symmetric URL to /v1/ads/campaigns/{campaignId}/status. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_set_id** | **String** | Platform ad set ID | [required] |
**update_ad_campaign_status_request** | [**UpdateAdCampaignStatusRequest**](UpdateAdCampaignStatusRequest.md) |  | [required] |

### Return type

[**models::UpdateAdSetStatus200Response**](updateAdSetStatus_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

