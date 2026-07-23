# \ReachAndFrequencyApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancel_rf_reservation**](ReachAndFrequencyApi.md#cancel_rf_reservation) | **DELETE** /v1/ads/rf-predictions/{predictionId} | Cancel a Reach & Frequency reservation
[**create_rf_prediction**](ReachAndFrequencyApi.md#create_rf_prediction) | **POST** /v1/ads/rf-predictions | Create a Reach & Frequency prediction
[**get_rf_prediction**](ReachAndFrequencyApi.md#get_rf_prediction) | **GET** /v1/ads/rf-predictions/{predictionId} | Read a Reach & Frequency prediction
[**reserve_rf_prediction**](ReachAndFrequencyApi.md#reserve_rf_prediction) | **POST** /v1/ads/rf-predictions/{predictionId}/reserve | Reserve a Reach & Frequency prediction



## cancel_rf_reservation

> cancel_rf_reservation(prediction_id, account_id, ad_account_id)
Cancel a Reach & Frequency reservation

Releases a RESERVATION's locked price and inventory. Unreserved predictions expire on their own.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**prediction_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |
**ad_account_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_rf_prediction

> models::CreateRfPrediction201Response create_rf_prediction(create_rf_prediction_request)
Create a Reach & Frequency prediction

Creates an R&F prediction — a QUOTE, nothing is bought and no ad entities are created. Provide a date range plus exactly one of `budgetAmount` (Meta predicts reach) or `reach` (Meta predicts the budget). The response carries the estimate and its allowed bounds (min/max budget and reach). Predictions expire on their own; to buy, reserve one via POST /v1/ads/rf-predictions/{predictionId}/reserve and pass the RESERVED id to POST /v1/ads/create with `buyingType: \"RESERVED\"`.  Reservation campaigns reject automatic placements, so omitted `placements` default to Facebook feed (+ Instagram stream when a linked IG professional account resolves); Instagram placements require that IG account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_rf_prediction_request** | [**CreateRfPredictionRequest**](CreateRfPredictionRequest.md) |  | [required] |

### Return type

[**models::CreateRfPrediction201Response**](createRfPrediction_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_rf_prediction

> models::CreateRfPrediction201Response get_rf_prediction(prediction_id, account_id, ad_account_id)
Read a Reach & Frequency prediction

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**prediction_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |
**ad_account_id** | **String** |  | [required] |

### Return type

[**models::CreateRfPrediction201Response**](createRfPrediction_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reserve_rf_prediction

> models::ReserveRfPrediction201Response reserve_rf_prediction(prediction_id, reserve_rf_prediction_request)
Reserve a Reach & Frequency prediction

Locks the quoted price + inventory until the returned `expiresAt` and mints a NEW prediction id — pass that RESERVED id (not the original) as `rfPredictionId` on POST /v1/ads/create. Release an unused reservation via DELETE.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**prediction_id** | **String** |  | [required] |
**reserve_rf_prediction_request** | [**ReserveRfPredictionRequest**](ReserveRfPredictionRequest.md) |  | [required] |

### Return type

[**models::ReserveRfPrediction201Response**](reserveRfPrediction_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

