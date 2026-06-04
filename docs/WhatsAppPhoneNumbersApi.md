# \WhatsAppPhoneNumbersApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_whats_app_number_info**](WhatsAppPhoneNumbersApi.md#get_whats_app_number_info) | **GET** /v1/whatsapp/number-info | Get number status
[**get_whats_app_number_kyc_form**](WhatsAppPhoneNumbersApi.md#get_whats_app_number_kyc_form) | **GET** /v1/whatsapp/phone-numbers/kyc | Get regulated-number KYC form spec
[**get_whats_app_phone_number**](WhatsAppPhoneNumbersApi.md#get_whats_app_phone_number) | **GET** /v1/whatsapp/phone-numbers/{phoneNumberId} | Get phone number
[**get_whats_app_phone_numbers**](WhatsAppPhoneNumbersApi.md#get_whats_app_phone_numbers) | **GET** /v1/whatsapp/phone-numbers | List phone numbers
[**list_whats_app_number_countries**](WhatsAppPhoneNumbersApi.md#list_whats_app_number_countries) | **GET** /v1/whatsapp/phone-numbers/countries | List offerable number countries
[**purchase_whats_app_phone_number**](WhatsAppPhoneNumbersApi.md#purchase_whats_app_phone_number) | **POST** /v1/whatsapp/phone-numbers/purchase | Purchase phone number
[**release_whats_app_phone_number**](WhatsAppPhoneNumbersApi.md#release_whats_app_phone_number) | **DELETE** /v1/whatsapp/phone-numbers/{phoneNumberId} | Release phone number
[**search_available_whats_app_numbers**](WhatsAppPhoneNumbersApi.md#search_available_whats_app_numbers) | **GET** /v1/whatsapp/phone-numbers/available | Search available numbers to purchase
[**submit_whats_app_number_kyc**](WhatsAppPhoneNumbersApi.md#submit_whats_app_number_kyc) | **POST** /v1/whatsapp/phone-numbers/kyc | Submit regulated-number KYC
[**upload_whats_app_number_kyc_document**](WhatsAppPhoneNumbersApi.md#upload_whats_app_number_kyc_document) | **POST** /v1/whatsapp/phone-numbers/kyc/upload-document | Upload a single regulated-number KYC document



## get_whats_app_number_info

> models::GetWhatsAppNumberInfo200Response get_whats_app_number_info(account_id)
Get number status

Live snapshot of a connected number straight from Meta: the phone-number node (display number, display name + approval, quality rating, messaging-limit tier, throughput, official-business badge, connection status, health_status) and its owning WhatsApp Business Account (name, business verification, timezone, health_status). Fetched live because Meta updates quality/tier/name/health over time; the call also refreshes the cached values shown on the connection card. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | [required] |

### Return type

[**models::GetWhatsAppNumberInfo200Response**](getWhatsAppNumberInfo_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_number_kyc_form

> models::GetWhatsAppNumberKycForm200Response get_whats_app_number_kyc_form(country, profile_id)
Get regulated-number KYC form spec

For a Tier 3/4 country, the fields the end customer must provide (Telnyx regulatory requirements) before a number can be ordered: text, date, address, or file (document) per requirement. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**country** | **String** |  | [required] |
**profile_id** | **String** |  | [required] |

### Return type

[**models::GetWhatsAppNumberKycForm200Response**](getWhatsAppNumberKycForm_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_phone_number

> models::GetWhatsAppPhoneNumber200Response get_whats_app_phone_number(phone_number_id)
Get phone number

Retrieve the current status of a purchased phone number. Poll this to track Meta pre-verification (US sync path) and, for regulated (Tier 3/4) numbers, the async lifecycle: pending_regulatory → active (or regulatory_declined). When a regulated number has an Onfido ID step, `onfidoVerificationUrl` appears here once the order is placed — forward it to the end user. (Or subscribe to the whatsapp.number.* webhooks instead of polling.) 

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


## list_whats_app_number_countries

> models::ListWhatsAppNumberCountries200Response list_whats_app_number_countries()
List offerable number countries

The WhatsApp number countries available to purchase, each with its flat monthly price (cents), regulatory tier, whether it needs end-user KYC (Tier 3/4), and whether outbound calling is available (not BIC-blocked). Drives the country picker. Tier-4 countries appear only when enabled. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListWhatsAppNumberCountries200Response**](listWhatsAppNumberCountries_200_response.md)

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


## search_available_whats_app_numbers

> models::SearchAvailableWhatsAppNumbers200Response search_available_whats_app_numbers(country, r#type, prefix, locality, contains, limit)
Search available numbers to purchase

Search the provider's inventory for numbers available to purchase in a country (default US). Optional filters narrow the results. The country must be offerable (see GET /v1/whatsapp/phone-numbers/countries). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**country** | Option<**String**> |  |  |[default to US]
**r#type** | Option<**String**> | Number type; defaults to the country's WhatsApp-safe type |  |
**prefix** | Option<**String**> | Area code |  |
**locality** | Option<**String**> | City |  |
**contains** | Option<**String**> | Pattern to match within the number |  |
**limit** | Option<**i32**> |  |  |[default to 20]

### Return type

[**models::SearchAvailableWhatsAppNumbers200Response**](searchAvailableWhatsAppNumbers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## submit_whats_app_number_kyc

> models::SubmitWhatsAppNumberKyc200Response submit_whats_app_number_kyc(submit_whats_app_number_kyc_request)
Submit regulated-number KYC

Submit the end customer's KYC (textual values, uploaded documents, address) for a Tier 3/4 country. Documents are streamed straight to the number provider and are not stored by Zernio. Builds + submits a regulatory requirement group and claims a pending_regulatory slot; the number is ordered + activated once the provider approves (asynchronous). A customer may hold several same-country numbers in review at once; a double-submit of the SAME attempt is deduped via `submissionId`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**submit_whats_app_number_kyc_request** | [**SubmitWhatsAppNumberKycRequest**](SubmitWhatsAppNumberKycRequest.md) |  | [required] |

### Return type

[**models::SubmitWhatsAppNumberKyc200Response**](submitWhatsAppNumberKyc_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upload_whats_app_number_kyc_document

> models::UploadWhatsAppNumberKycDocument200Response upload_whats_app_number_kyc_document(x_filename, body)
Upload a single regulated-number KYC document

Upload ONE document and get back its provider document id, to reference from POST /v1/whatsapp/phone-numbers/kyc via `documents[].documentId`. Send the RAW file bytes as the request body (not base64); put the filename in the `X-Filename` header. Uploading documents one-per-request keeps each request under the ~4.5MB body limit. The document streams straight to the number provider and is not stored by Zernio. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**x_filename** | **String** | URL-encoded original filename. | [required] |
**body** | **std::path::PathBuf** |  | [required] |

### Return type

[**models::UploadWhatsAppNumberKycDocument200Response**](uploadWhatsAppNumberKycDocument_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/octet-stream
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

