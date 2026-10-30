# \AdCampaignResultsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_campaign_results_upload**](AdCampaignResultsApi.md#get_campaign_results_upload) | **GET** /v1/ads/campaign-results/uploads/{uploadId} | Check a results upload
[**list_campaign_result_metrics**](AdCampaignResultsApi.md#list_campaign_result_metrics) | **GET** /v1/ads/campaign-results/metrics | List your result metrics
[**list_campaign_results**](AdCampaignResultsApi.md#list_campaign_results) | **GET** /v1/ads/campaign-results | List your results per campaign
[**set_campaign_result_metric**](AdCampaignResultsApi.md#set_campaign_result_metric) | **PUT** /v1/ads/campaign-results/metrics/{key} | Name a result metric
[**upload_campaign_results**](AdCampaignResultsApi.md#upload_campaign_results) | **POST** /v1/ads/campaign-results | Upload your results per campaign



## get_campaign_results_upload

> models::GetCampaignResultsUpload200Response get_campaign_results_upload(upload_id)
Check a results upload

How an upload was matched: rows matched and unmatched, and up to 100 unmatched rows with why (`no_campaign` or `ambiguous`).  `status` turns `done` once every row is processed, usually within seconds. Uploads are kept for 30 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**upload_id** | **String** |  | [required] |

### Return type

[**models::GetCampaignResultsUpload200Response**](getCampaignResultsUpload_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_campaign_result_metrics

> models::ListCampaignResultMetrics200Response list_campaign_result_metrics()
List your result metrics

The metric keys your team has sent, with their label and kind. A new key appears as a `count` labelled from the key; name it with `PUT /v1/ads/campaign-results/metrics/{key}`. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListCampaignResultMetrics200Response**](listCampaignResultMetrics_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_campaign_results

> models::ListCampaignResults200Response list_campaign_results(from_date, to_date, campaign_ids, limit, cursor)
List your results per campaign

Your results summed per campaign over a date range, one entry per campaign with every metric it has, for the ad accounts your key can see. Each day counts its newest value only.  Paginated by campaign: pass `nextCursor` back as `cursor` until it is null. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from_date** | **String** |  | [required] |
**to_date** | **String** | Inclusive. At most 400 days after `fromDate`. | [required] |
**campaign_ids** | Option<**String**> | Comma-separated platform campaign ids, at most 500. Omit for all campaigns. |  |
**limit** | Option<**i32**> | Campaigns per page. |  |[default to 100]
**cursor** | Option<**String**> | `nextCursor` from the previous page. |  |

### Return type

[**models::ListCampaignResults200Response**](listCampaignResults_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_campaign_result_metric

> models::SetCampaignResultMetric200Response set_campaign_result_metric(key, set_campaign_result_metric_request)
Name a result metric

Sets a metric key's label and kind: `count` for things you count (leads, sales) or `money` with its currency (revenue). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**key** | **String** |  | [required] |
**set_campaign_result_metric_request** | [**SetCampaignResultMetricRequest**](SetCampaignResultMetricRequest.md) |  | [required] |

### Return type

[**models::SetCampaignResultMetric200Response**](setCampaignResultMetric_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upload_campaign_results

> models::UploadCampaignResults202Response upload_campaign_results(upload_campaign_results_request, idempotency_key)
Upload your results per campaign

Sends your own daily numbers per campaign (qualified leads, sales, revenue...) so rules and reports can use them next to spend.  Name each row's campaign by `campaignId`, `utmCampaign` or `campaignName`. Rows are matched in the background: the `202` returns an `uploadId`, and `Location` points to `GET /v1/ads/campaign-results/uploads/{uploadId}`.  Re-sending a day replaces it. Send an `Idempotency-Key` to retry safely. Limits per team: 60 requests and 20,000 rows per hour, 512 KB per request. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**upload_campaign_results_request** | [**UploadCampaignResultsRequest**](UploadCampaignResultsRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | A retry with the same key and body replays the first response instead of uploading twice. |  |

### Return type

[**models::UploadCampaignResults202Response**](uploadCampaignResults_202_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

