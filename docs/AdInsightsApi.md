# \AdInsightsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_ad_insights_report**](AdInsightsApi.md#create_ad_insights_report) | **POST** /v1/ads/insights/reports | Submit an async insights report run
[**get_ad_analytics**](AdInsightsApi.md#get_ad_analytics) | **GET** /v1/ads/{adId}/analytics | Get ad analytics
[**get_ad_insights_report**](AdInsightsApi.md#get_ad_insights_report) | **GET** /v1/ads/insights/reports/{reportRunId} | Poll an async insights report run
[**get_campaign_analytics**](AdInsightsApi.md#get_campaign_analytics) | **GET** /v1/ads/campaigns/{campaignId}/analytics | Get campaign analytics
[**query_ad_insights**](AdInsightsApi.md#query_ad_insights) | **GET** /v1/ads/insights | Flexible live insights query



## create_ad_insights_report

> models::CreateAdInsightsReport202Response create_ad_insights_report(create_ad_insights_report_request)
Submit an async insights report run

Submits an asynchronous Meta insights report. Same query surface as GET /v1/ads/insights, but in the JSON body; Meta processes the report server-side, which is the right choice for long ranges or large accounts where the sync query is slow or rate-limited. Returns a `reportRunId` to poll via GET /v1/ads/insights/reports/{reportRunId}. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_ad_insights_report_request** | [**CreateAdInsightsReportRequest**](CreateAdInsightsReportRequest.md) |  | [required] |

### Return type

[**models::CreateAdInsightsReport202Response**](createAdInsightsReport_202_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_analytics

> models::GetAdAnalytics200Response get_ad_analytics(ad_id, from_date, to_date, breakdowns)
Get ad analytics

Returns detailed performance analytics for an ad. Includes summary metrics, a daily timeline over the requested date range, and optional demographic breakdowns (Meta and TikTok only). If no date range is provided, defaults to the last 90 days. Date range is capped at 730 days max. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ad_id** | **String** |  | [required] |
**from_date** | Option<**String**> | Start of date range (YYYY-MM-DD). Defaults to 90 days ago. |  |
**to_date** | Option<**String**> | End of date range (YYYY-MM-DD). Defaults to today. Max 730-day range. |  |
**breakdowns** | Option<**String**> | Comma-separated breakdown dimensions.  **Meta**: age, gender, country, publisher_platform, device_platform, region.  **TikTok**: gender, age, country_code, platform, ac, language.  **LinkedIn** (firmographics): job_title, job_function, seniority, industry, company, company_size, country, region. Rows carry the raw pivot `value` plus a resolved `name`. LinkedIn serves these aggregated over the whole range, delays the data 12-24h, and omits segments with fewer than 3 events.  |  |

### Return type

[**models::GetAdAnalytics200Response**](getAdAnalytics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_insights_report

> models::GetAdInsightsReport200Response get_ad_insights_report(report_run_id, account_id, limit, after)
Poll an async insights report run

Status and results for a report run created via POST /v1/ads/insights/reports. While the job runs, returns `status` and `percentCompletion`. Once `status` is \"Job Completed\" the response also carries a `data` page, cursor-paginated via `limit` / `after`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**report_run_id** | **String** |  | [required] |
**account_id** | **String** | Zernio SocialAccount id used to resolve the Meta token (must be the same connection that created the run). | [required] |
**limit** | Option<**i32**> |  |  |[default to 25]
**after** | Option<**String**> |  |  |

### Return type

[**models::GetAdInsightsReport200Response**](getAdInsightsReport_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_campaign_analytics

> models::GetCampaignAnalytics200Response get_campaign_analytics(campaign_id, platform, from_date, to_date, breakdowns)
Get campaign analytics

Returns performance analytics for a whole campaign in one call: summary metrics, a daily timeline over the requested date range (summed across the campaign's ads), and optional demographic breakdowns. Breakdowns are fetched live from Meta at the campaign level (one call per dimension, no per-ad fan-out), so an agency dashboard gets campaign-level age/gender/etc. without summing thousands of per-ad reads. `campaignId` is the platform campaign id; pass `platform` when a campaign id could be ambiguous across platforms. If no date range is provided, defaults to the last 90 days. Date range is capped at 730 days max. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**campaign_id** | **String** | Platform campaign id (platformCampaignId). | [required] |
**platform** | Option<**String**> | Disambiguate when the campaign id exists across platforms (e.g. facebook, instagram). |  |
**from_date** | Option<**String**> | Start of date range (YYYY-MM-DD). Defaults to 90 days ago. |  |
**to_date** | Option<**String**> | End of date range (YYYY-MM-DD). Defaults to today. Max 730-day range. |  |
**breakdowns** | Option<**String**> | Comma-separated breakdown dimensions.  **Meta**: age, gender, country, publisher_platform, device_platform, region, platform_position, impression_device, video_asset, image_asset, body_asset, title_asset.  **LinkedIn** (firmographics): job_title, job_function, seniority, industry, company, company_size, country, region. Rows carry the raw pivot `value` plus a resolved `name`. LinkedIn serves these aggregated over the whole range, delays the data 12-24h, and omits segments with fewer than 3 events.  |  |

### Return type

[**models::GetCampaignAnalytics200Response**](getCampaignAnalytics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## query_ad_insights

> models::QueryAdInsights200Response query_ad_insights(account_id, object_id, level, fields, breakdowns, action_breakdowns, action_attribution_windows, action_report_time, use_unified_attribution_setting, filtering, date_preset, from_date, to_date, time_increment, limit, after)
Flexible live insights query

Live, flexible insights query against Meta's Graph API. Unlike GET /v1/ads/{adId}/analytics (fixed metric set, cached), this forwards caller-chosen `fields`, `breakdowns` and `filtering` to any Meta insights node and returns Meta's rows verbatim.  `objectId` selects the node: an ad account, campaign, ad set or ad platform id. `level` sets row granularity independently of the node.  Semantic validation is Meta's: an unknown field or invalid breakdown combination returns a 400 carrying Meta's message. For long ranges or agency-scale accounts prefer the async variant (POST /v1/ads/insights/reports). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | [required] |
**object_id** | **String** | Meta insights node: act_<n>, campaign id, ad set id or ad id. | [required] |
**level** | Option<**String**> | Row granularity |  |
**fields** | Option<**String**> | Comma-separated Graph insights fields (e.g. spend,impressions,frequency,website_purchase_roas). Omitted = Meta's default set. |  |
**breakdowns** | Option<**String**> | Comma-separated Graph breakdowns (e.g. age,gender or publisher_platform). |  |
**action_breakdowns** | Option<**String**> | Comma-separated Graph action breakdowns. Segments the actions[] arrays in each row. |  |
**action_attribution_windows** | Option<**String**> | Comma-separated Meta attribution windows. Action values are returned keyed per window. |  |
**action_report_time** | Option<**String**> | When actions are counted: impression, conversion or mixed. |  |
**use_unified_attribution_setting** | Option<**bool**> | Use the ad sets' own attribution settings for action counting. |  |
**filtering** | Option<**String**> | JSON array of Meta filter objects: [{\"field\", \"operator\", \"value\"}]. Applied server-side by Meta. |  |
**date_preset** | Option<**String**> | Meta date_preset (e.g. last_7d, last_30d, this_month). Mutually exclusive with fromDate/toDate. |  |
**from_date** | Option<**String**> | Start of range (YYYY-MM-DD); requires toDate. |  |
**to_date** | Option<**String**> | End of range (YYYY-MM-DD); requires fromDate. |  |
**time_increment** | Option<**String**> | Days per row (1-90), monthly, or all_days. |  |
**limit** | Option<**i32**> | Rows per page |  |[default to 25]
**after** | Option<**String**> | Cursor from paging.after of the previous page. |  |

### Return type

[**models::QueryAdInsights200Response**](queryAdInsights_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

