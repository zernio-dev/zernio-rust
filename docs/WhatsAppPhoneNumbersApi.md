# \WhatsAppPhoneNumbersApi

All URIs are relative to *https://getlate.dev/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_preverified_whats_app_numbers**](WhatsAppPhoneNumbersApi.md#get_preverified_whats_app_numbers) | **GET** /v1/whatsapp/phone-numbers/preverified | Get pre-verified numbers
[**get_whats_app_phone_number**](WhatsAppPhoneNumbersApi.md#get_whats_app_phone_number) | **GET** /v1/whatsapp/phone-numbers/{phoneNumberId} | Get phone number
[**get_whats_app_phone_numbers**](WhatsAppPhoneNumbersApi.md#get_whats_app_phone_numbers) | **GET** /v1/whatsapp/phone-numbers | List phone numbers
[**purchase_whats_app_phone_number**](WhatsAppPhoneNumbersApi.md#purchase_whats_app_phone_number) | **POST** /v1/whatsapp/phone-numbers/purchase | Purchase phone number
[**release_whats_app_phone_number**](WhatsAppPhoneNumbersApi.md#release_whats_app_phone_number) | **DELETE** /v1/whatsapp/phone-numbers/{phoneNumberId} | Release phone number
[**request_whats_app_verification_code**](WhatsAppPhoneNumbersApi.md#request_whats_app_verification_code) | **POST** /v1/whatsapp/phone-numbers/{phoneNumberId}/request-code | Request OTP
[**search_available_whats_app_numbers**](WhatsAppPhoneNumbersApi.md#search_available_whats_app_numbers) | **GET** /v1/whatsapp/phone-numbers/available | Search available numbers
[**verify_whats_app_phone_number**](WhatsAppPhoneNumbersApi.md#verify_whats_app_phone_number) | **POST** /v1/whatsapp/phone-numbers/{phoneNumberId}/verify | Verify OTP



## get_preverified_whats_app_numbers

> models::GetPreverifiedWhatsAppNumbers200Response get_preverified_whats_app_numbers(profile_id)
Get pre-verified numbers

Returns the user's pre-verified phone number IDs that are ready for OTP-free Embedded Signup. Only returns numbers with verified Meta status and non-expired verification. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | **String** | Profile ID to filter by | [required] |

### Return type

[**models::GetPreverifiedWhatsAppNumbers200Response**](getPreverifiedWhatsAppNumbers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_phone_number

> models::GetWhatsAppPhoneNumber200Response get_whats_app_phone_number(phone_number_id)
Get phone number

Retrieve the current status of a purchased phone number. Used to poll for Meta pre-verification completion after purchase. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**phone_number_id** | **String** | Phone number record ID | [required] |

### Return type

[**models::GetWhatsAppPhoneNumber200Response**](getWhatsAppPhoneNumber_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_phone_numbers

> models::GetWhatsAppPhoneNumbers200Response get_whats_app_phone_numbers(status, profile_id)
List phone numbers

List all WhatsApp phone numbers purchased by the authenticated user. By default, released numbers are excluded. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**status** | Option<**String**> | Filter by status (by default excludes released numbers) |  |
**profile_id** | Option<**String**> | Filter by profile |  |

### Return type

[**models::GetWhatsAppPhoneNumbers200Response**](getWhatsAppPhoneNumbers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## purchase_whats_app_phone_number

> models::PurchaseWhatsAppPhoneNumber200Response purchase_whats_app_phone_number(purchase_whats_app_phone_number_request)
Purchase phone number

Initiate purchasing a WhatsApp phone number. Payment-first flow: the user does not pick a specific number. The system either creates a Stripe Checkout Session (first number) or increments the existing subscription quantity and provisions inline (subsequent numbers).  Requires a paid plan. The maximum number of phone numbers is determined by the user's plan. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**purchase_whats_app_phone_number_request** | [**PurchaseWhatsAppPhoneNumberRequest**](PurchaseWhatsAppPhoneNumberRequest.md) |  | [required] |

### Return type

[**models::PurchaseWhatsAppPhoneNumber200Response**](purchaseWhatsAppPhoneNumber_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## release_whats_app_phone_number

> models::ReleaseWhatsAppPhoneNumber200Response release_whats_app_phone_number(phone_number_id)
Release phone number

Release a purchased phone number. This will: 1. Disconnect any linked WhatsApp social account 2. Decrement the Stripe subscription quantity (or cancel if last number) 3. Release the number from Telnyx 4. Mark the number as released 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**phone_number_id** | **String** | Phone number record ID | [required] |

### Return type

[**models::ReleaseWhatsAppPhoneNumber200Response**](releaseWhatsAppPhoneNumber_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## request_whats_app_verification_code

> models::RequestWhatsAppVerificationCode200Response request_whats_app_verification_code(phone_number_id, request_whats_app_verification_code_request)
Request OTP

Request a new OTP verification code from Meta for a pre-verified phone number. Useful when the initial SMS did not arrive or when re-verifying before the 90-day expiry. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**phone_number_id** | **String** | Phone number record ID | [required] |
**request_whats_app_verification_code_request** | Option<[**RequestWhatsAppVerificationCodeRequest**](RequestWhatsAppVerificationCodeRequest.md)> |  |  |

### Return type

[**models::RequestWhatsAppVerificationCode200Response**](requestWhatsAppVerificationCode_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_available_whats_app_numbers

> models::SearchAvailableWhatsAppNumbers200Response search_available_whats_app_numbers(prefix, locality, contains, limit)
Search available numbers

Search for available US phone numbers that can be purchased for WhatsApp Business. Requires a paid plan. Numbers are sourced from Telnyx. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**prefix** | Option<**String**> | Area code to search (e.g., \"212\" for New York) |  |
**locality** | Option<**String**> | City name (e.g., \"New York\") |  |
**contains** | Option<**String**> | Pattern to match within the phone number |  |
**limit** | Option<**i32**> | Maximum results (default 20, max 100) |  |[default to 20]

### Return type

[**models::SearchAvailableWhatsAppNumbers200Response**](searchAvailableWhatsAppNumbers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## verify_whats_app_phone_number

> models::VerifyWhatsAppPhoneNumber200Response verify_whats_app_phone_number(phone_number_id, verify_whats_app_phone_number_request)
Verify OTP

Manually verify a phone number by entering the OTP code received via SMS or voice call. This is a fallback for when the auto-verification webhook does not capture the code. Verification is valid for 90 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**phone_number_id** | **String** | Phone number record ID | [required] |
**verify_whats_app_phone_number_request** | [**VerifyWhatsAppPhoneNumberRequest**](VerifyWhatsAppPhoneNumberRequest.md) |  | [required] |

### Return type

[**models::VerifyWhatsAppPhoneNumber200Response**](verifyWhatsAppPhoneNumber_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

