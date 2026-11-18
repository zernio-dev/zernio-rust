# \AdCampaignResultsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_campaign_result_events**](AdCampaignResultsApi.md#get_campaign_result_events) | **GET** /v1/ads/campaign-results/events | List the events that count as campaign results
[**get_campaign_results_totals**](AdCampaignResultsApi.md#get_campaign_results_totals) | **GET** /v1/ads/campaign-results/totals | Get your results totals
[**get_campaign_results_upload**](AdCampaignResultsApi.md#get_campaign_results_upload) | **GET** /v1/ads/campaign-results/uploads/{uploadId} | Check a results upload
[**get_tag_new_ads**](AdCampaignResultsApi.md#get_tag_new_ads) | **GET** /v1/ads/campaign-results/tag-new-ads | Get the Tag new ads setting
[**list_campaign_result_metrics**](AdCampaignResultsApi.md#list_campaign_result_metrics) | **GET** /v1/ads/campaign-results/metrics | List your result metrics
[**list_campaign_results**](AdCampaignResultsApi.md#list_campaign_results) | **GET** /v1/ads/campaign-results | List your results per campaign
[**set_campaign_result_events**](AdCampaignResultsApi.md#set_campaign_result_events) | **PUT** /v1/ads/campaign-results/events | Choose the events that count as campaign results
[**set_campaign_result_metric**](AdCampaignResultsApi.md#set_campaign_result_metric) | **PUT** /v1/ads/campaign-results/metrics/{key} | Name a result metric or define a formula
[**set_tag_new_ads**](AdCampaignResultsApi.md#set_tag_new_ads) | **PUT** /v1/ads/campaign-results/tag-new-ads | Turn Tag new ads on or off
[**upload_campaign_results**](AdCampaignResultsApi.md#upload_campaign_results) | **POST** /v1/ads/campaign-results | Upload your results per campaign



## get_campaign_result_events

> models::GetCampaignResultEvents200Response get_campaign_result_events()
List the events that count as campaign results

The names of the events sent to `POST /v1/events` that your team counts as campaign results. Only these are tied to a campaign when they arrive. Until you choose, they are `Purchase`, `Lead` and `QualifiedLead`. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::GetCampaignResultEvents200Response**](getCampaignResultEvents_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_campaign_results_totals

> models::GetCampaignResultsTotals200Response get_campaign_results_totals(from_date, to_date, model, ad_account_ids)
Get your results totals

Each metric you send summed over a date range across every campaign of the ad accounts your key can see, or of the ones you name. Each day counts its newest uploaded value only, plus the events sent to `POST /v1/events` that are tied to a campaign.  An event counts here up to 15 minutes after it arrives.  Formulas are not computed here, since they also read the platform's numbers: apply one to these totals and the account's spend for the same range, or read it per campaign from `GET /v1/ads/tree?results=true`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from_date** | **String** |  | [required] |
**to_date** | **String** | Inclusive. At most 400 days after `fromDate`. | [required] |
**model** | Option<**String**> | Attribution model your stored sales and leads count under. `last_click` (default) counts each event whole for the campaign it matched. The others split it across the campaigns of its earlier touches, so counts and revenue can be fractional. Uploads read the same under every model. |  |[default to last_click]
**ad_account_ids** | Option<**String**> | Comma-separated platform ad account ids, at most 100. Omit for every ad account your key can see. |  |

### Return type

[**models::GetCampaignResultsTotals200Response**](getCampaignResultsTotals_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_campaign_results_upload

> models::GetCampaignResultsUpload200Response get_campaign_results_upload(upload_id)
Check a results upload

How an upload was matched: rows matched and unmatched, and up to 100 unmatched rows with why (`no_campaign` or `ambiguous`).  `status` turns `done` once every row is processed, usually within seconds. Uploads are kept for 30 days.  A `failed` upload says why in `failureReason`. Send it again: re-sending a day replaces it, so nothing is counted twice. 

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


## get_tag_new_ads

> models::GetTagNewAds200Response get_tag_new_ads()
Get the Tag new ads setting

Whether new Meta and Google ads created through Zernio carry the Zernio ad tag (`zrn=<platform ad id>` on the landing URL) when the create request does not set `tracking.zernioTag`. Off until you turn it on. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::GetTagNewAds200Response**](getTagNewAds_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_campaign_result_metrics

> models::ListCampaignResultMetrics200Response list_campaign_result_metrics()
List your result metrics

The metric keys your team has sent, with their label and kind, then the formulas: your own and the built-in ones (`cac_percent`, `cost_per_sale`, `cost_per_qualified_lead`, `lead_to_sale`, `qualified_rate`). A new key appears as a `count` labelled from the key; name it, or define a formula, with `PUT /v1/ads/campaign-results/metrics/{key}`. 

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

> models::ListCampaignResults200Response list_campaign_results(from_date, to_date, model, campaign_ids, limit, cursor)
List your results per campaign

Your results summed per campaign over a date range, one entry per campaign with every metric it has, for the ad accounts your key can see. Each day counts its newest uploaded value only, plus the events sent to `POST /v1/events` that are tied to the campaign (`sales`, `revenue`, `leads`, `qualified_leads`).  An event counts here up to 15 minutes after it arrives.  Paginated by campaign: pass `nextCursor` back as `cursor` until it is null. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**from_date** | **String** |  | [required] |
**to_date** | **String** | Inclusive. At most 400 days after `fromDate`. | [required] |
**model** | Option<**String**> | Attribution model your stored sales and leads count under. `last_click` (default) counts each event whole for the campaign it matched. The others split it across the campaigns of its earlier touches, so counts and revenue can be fractional. Uploads read the same under every model. |  |[default to last_click]
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


## set_campaign_result_events

> models::SetCampaignResultEvents200Response set_campaign_result_events(set_campaign_result_events_request)
Choose the events that count as campaign results

Sets which stored events are tied to a campaign when they arrive and add to its results.  `Purchase` adds `sales` and `revenue`, `Lead` adds `leads` and `QualifiedLead` adds `qualified_leads`. Any other event adds 1 per event to a metric keyed `event_` plus its name in lowercase, e.g. `event_completeregistration`, which formulas and rules can read.  Events stored before the change keep how they were counted. Send `null` to go back to `Purchase`, `Lead` and `QualifiedLead`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**set_campaign_result_events_request** | [**SetCampaignResultEventsRequest**](SetCampaignResultEventsRequest.md) |  | [required] |

### Return type

[**models::SetCampaignResultEvents200Response**](setCampaignResultEvents_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_campaign_result_metric

> models::SetCampaignResultMetric200Response set_campaign_result_metric(key, set_campaign_result_metric_request)
Name a result metric or define a formula

Sets a metric key's label and kind: `count` for things you count (leads, sales), `money` with its currency (revenue), `percent` or `ratio`.  Send `formula` to make it a computed metric: `+ - * /` and parentheses over `spend`, `impressions`, `clicks`, `conversions`, `purchase_value` and the metrics you send, at most 200 characters. A formula cannot read another formula.  It is computed per campaign over the summed values of the range, and has no value when an input is missing or a division is by zero. 

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


## set_tag_new_ads

> models::SetTagNewAds200Response set_tag_new_ads(set_tag_new_ads_request)
Turn Tag new ads on or off

With `enabled: true`, every new Meta and Google ad created through `POST /v1/ads/create` carries `zrn=<platform ad id>` on its landing URL, so the conversions it brings are tied to its campaign. A request that sets `tracking.zernioTag` keeps its own choice.  The same rules as `tracking.zernioTag` apply: lead forms, call ads, existing creatives and app promotion are skipped, and a Google ad is tagged only when it inherits no final URL suffix. Existing ads are never changed. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**set_tag_new_ads_request** | [**SetTagNewAdsRequest**](SetTagNewAdsRequest.md) |  | [required] |

### Return type

[**models::SetTagNewAds200Response**](setTagNewAds_200_response.md)

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

