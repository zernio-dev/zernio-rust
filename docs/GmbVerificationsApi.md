# \GmbVerificationsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**complete_google_business_verification**](GmbVerificationsApi.md#complete_google_business_verification) | **POST** /v1/accounts/{accountId}/gmb-verifications/{verificationId}/complete | Complete a verification
[**fetch_google_business_verification_options**](GmbVerificationsApi.md#fetch_google_business_verification_options) | **POST** /v1/accounts/{accountId}/gmb-verifications/options | Fetch verification options
[**get_google_business_verifications**](GmbVerificationsApi.md#get_google_business_verifications) | **GET** /v1/accounts/{accountId}/gmb-verifications | Get verification state
[**start_google_business_verification**](GmbVerificationsApi.md#start_google_business_verification) | **POST** /v1/accounts/{accountId}/gmb-verifications | Start a verification



## complete_google_business_verification

> models::StartGoogleBusinessVerification200Response complete_google_business_verification(account_id, verification_id, complete_google_business_verification_request, location_id)
Complete a verification

Completes a PENDING verification by submitting the PIN/code Google sent the business (postcard code, SMS PIN, etc.). On success the verification moves to COMPLETED.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio account ID (from /v1/accounts) | [required] |
**verification_id** | **String** | The last segment of a verification `name` from GET /gmb-verifications. | [required] |
**complete_google_business_verification_request** | [**CompleteGoogleBusinessVerificationRequest**](CompleteGoogleBusinessVerificationRequest.md) |  | [required] |
**location_id** | Option<**String**> | Override which location to target. If omitted, uses the account's selected location. |  |

### Return type

[**models::StartGoogleBusinessVerification200Response**](startGoogleBusinessVerification_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## fetch_google_business_verification_options

> models::FetchGoogleBusinessVerificationOptions200Response fetch_google_business_verification_options(account_id, fetch_google_business_verification_options_request, location_id)
Fetch verification options

Reports the verification methods Google currently offers for the location. Non-mutating (nothing is sent to the business). `languageCode` is required; service-area (\"CUSTOMER_LOCATION_ONLY\") businesses also require `context.address`, otherwise Google returns 400.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio account ID (from /v1/accounts) | [required] |
**fetch_google_business_verification_options_request** | [**FetchGoogleBusinessVerificationOptionsRequest**](FetchGoogleBusinessVerificationOptionsRequest.md) |  | [required] |
**location_id** | Option<**String**> | Override which location to query. If omitted, uses the account's selected location. |  |

### Return type

[**models::FetchGoogleBusinessVerificationOptions200Response**](fetchGoogleBusinessVerificationOptions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_google_business_verifications

> models::GetGoogleBusinessVerifications200Response get_google_business_verifications(account_id, location_id)
Get verification state

Returns the location's Voice of Merchant state plus its verification history. `voiceOfMerchantState.hasVoiceOfMerchant` tells you whether the listing is verified and published; when it is false, `verify` reports whether a verification is already pending. Each entry in `verifications` has a `state` of PENDING, COMPLETED, or FAILED.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio account ID (from /v1/accounts) | [required] |
**location_id** | Option<**String**> | Override which location to query. If omitted, uses the account's selected location. Use GET /gmb-locations to list valid IDs. |  |

### Return type

[**models::GetGoogleBusinessVerifications200Response**](getGoogleBusinessVerifications_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## start_google_business_verification

> models::StartGoogleBusinessVerification200Response start_google_business_verification(account_id, start_google_business_verification_request, location_id)
Start a verification

Starts a verification for the location. This is a mutating action: depending on `method`, Google mails a postcard, places a call, or sends an SMS/email to the business. Submit the resulting code with POST /gmb-verifications/{verificationId}/complete. Use POST /gmb-verifications/options first to discover which methods are eligible.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The Zernio account ID (from /v1/accounts) | [required] |
**start_google_business_verification_request** | [**StartGoogleBusinessVerificationRequest**](StartGoogleBusinessVerificationRequest.md) |  | [required] |
**location_id** | Option<**String**> | Override which location to target. If omitted, uses the account's selected location. |  |

### Return type

[**models::StartGoogleBusinessVerification200Response**](startGoogleBusinessVerification_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

