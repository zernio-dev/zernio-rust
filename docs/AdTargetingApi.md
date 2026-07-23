# \AdTargetingApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**estimate_ad_reach**](AdTargetingApi.md#estimate_ad_reach) | **POST** /v1/ads/targeting/reach-estimate | Estimate audience reach
[**get_linked_in_bid_pricing**](AdTargetingApi.md#get_linked_in_bid_pricing) | **POST** /v1/ads/targeting/bid-pricing | Suggested bid and budget bounds
[**get_linked_in_supply_forecast**](AdTargetingApi.md#get_linked_in_supply_forecast) | **POST** /v1/ads/targeting/supply-forecast | Impressions, clicks and spend forecast
[**search_ad_interests**](AdTargetingApi.md#search_ad_interests) | **GET** /v1/ads/interests | Search targeting interests
[**search_ad_targeting**](AdTargetingApi.md#search_ad_targeting) | **GET** /v1/ads/targeting/search | Search targeting options



## estimate_ad_reach

> models::EstimateAdReach200Response estimate_ad_reach(estimate_ad_reach_request)
Estimate audience reach

Returns a normalized pre-flight audience-size estimate for a targeting spec, before any campaign is created. Backed by each platform's native reach API (Meta `delivery_estimate`, LinkedIn `audienceCounts`, X `audience_summary`, Pinterest `audience_sizing`).  Platforms without a usable pre-flight reach API (Google Search/Display, TikTok) return `available: false` with no bounds, so clients can hide or grey out the estimate rather than treat the absence as an error. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**estimate_ad_reach_request** | [**EstimateAdReachRequest**](EstimateAdReachRequest.md) |  | [required] |

### Return type

[**models::EstimateAdReach200Response**](estimateAdReach_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_linked_in_bid_pricing

> models::GetLinkedInBidPricing200Response get_linked_in_bid_pricing(get_linked_in_bid_pricing_request)
Suggested bid and budget bounds

LinkedIn-only. Returns the suggested bid and bid limits for a targeting spec, plus the daily-budget bounds LinkedIn will accept. Use it before creating a campaign to pick a bid inside the allowed range and warn the user if their daily budget is below the minimum. Wraps LinkedIn's `adBudgetPricing` finder.  Non-LinkedIn accounts return `available: false` so clients can hide the pricing UI without treating it as a failure. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**get_linked_in_bid_pricing_request** | [**GetLinkedInBidPricingRequest**](GetLinkedInBidPricingRequest.md) |  | [required] |

### Return type

[**models::GetLinkedInBidPricing200Response**](getLinkedInBidPricing_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_linked_in_supply_forecast

> models::GetLinkedInSupplyForecast200Response get_linked_in_supply_forecast(get_linked_in_supply_forecast_request)
Impressions, clicks and spend forecast

LinkedIn-only. Forecasted impressions, clicks, spend and ~20 other metrics for a targeting spec over a time range. Wraps LinkedIn's `adSupplyForecasts` finder.  Each returned series carries a `metricType` (IMPRESSION, CLICK, SPENDING, MAX_POTENTIAL_BUDGET, COST_PER_MILLION_IMPRESSIONS, ...) and a `granularity` (DAILY, SEVEN_DAY, THIRTY_DAY, CUSTOM). LinkedIn caps the daily spending forecast at 1.2x the daily budget and returns 0 once the total budget is exhausted.  Non-LinkedIn accounts return `available: false`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**get_linked_in_supply_forecast_request** | [**GetLinkedInSupplyForecastRequest**](GetLinkedInSupplyForecastRequest.md) |  | [required] |

### Return type

[**models::GetLinkedInSupplyForecast200Response**](getLinkedInSupplyForecast_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_ad_interests

> models::SearchAdInterests200Response search_ad_interests(q, account_id)
Search targeting interests

Deprecated alias for `GET /v1/ads/targeting/search?dimension=interest`. Kept for backward compatibility, it returns the legacy `{ interests: [...] }` shape rather than the normalized `{ results: [...] }`. New integrations should use `GET /v1/ads/targeting/search` with `dimension=interest`. 

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


## search_ad_targeting

> models::SearchAdTargeting200Response search_ad_targeting(account_id, q, dimension, geo_type, country_code, limit)
Search targeting options

Resolve a human-readable query into the platform's opaque targeting ids used in the `TargetingSpec` (`countries`/`regions`/`cities`/`zips`/`metros` geo keys, and `interests`/`behaviors` entity ids) on `POST /v1/ads/create`, `POST /v1/ads/targeting/reach-estimate`, and `saved_targeting` audiences.  The `dimension` param selects what is searched, `geo` (locations, further scoped by `geoType`), `interest`, `behavior`, or `income`. Availability of each dimension varies by platform (e.g. behaviours are Meta/TikTok only). Results are normalized across platforms into a single shape, so the same client code consumes Meta, TikTok, LinkedIn, X, Pinterest, and Google results.  TikTok geo searches return every matching level in one list (`type` is `country`, `region`, `city`, `district`, or `metro` for DMA areas) — `geoType` is not applied. Results are scoped to the advertiser's targetable markets, and every id is usable in `regions`/`cities`/`metros` keys on `POST /v1/ads/create`.  For geo queries, `q` should contain only the locality name (e.g. `\"Amsterdam\"`, not `\"Amsterdam, NL\"`). Use `countryCode` to disambiguate. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Social account ID (a connected account on the target ad platform). | [required] |
**q** | **String** | Search query. For geo, the locality name only (no region/country suffix). | [required] |
**dimension** | Option<**String**> | What to search. `geo` resolves locations (scope further with `geoType`), `interest`/`behavior` resolve audience entities, `income` resolves income-tier options. Defaults to `interest` for backward compatibility with the deprecated /v1/ads/interests alias. |  |[default to interest]
**geo_type** | Option<**String**> | Only used when `dimension=geo`. The kind of location to resolve. Defaults to `city`. |  |[default to city]
**country_code** | Option<**String**> | ISO 3166-1 alpha-2 country code (e.g. NL) to scope a geo search. |  |
**limit** | Option<**i32**> | Maximum results to return. |  |[default to 25]

### Return type

[**models::SearchAdTargeting200Response**](searchAdTargeting_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

