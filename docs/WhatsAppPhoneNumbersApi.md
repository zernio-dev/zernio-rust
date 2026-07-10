# \WhatsAppPhoneNumbersApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**check_whats_app_number_availability**](WhatsAppPhoneNumbersApi.md#check_whats_app_number_availability) | **GET** /v1/whatsapp/phone-numbers/availability | Check country availability
[**create_whats_app_number_kyc_link**](WhatsAppPhoneNumbersApi.md#create_whats_app_number_kyc_link) | **POST** /v1/whatsapp/phone-numbers/kyc/share | Create a hosted KYC link
[**get_whats_app_number_info**](WhatsAppPhoneNumbersApi.md#get_whats_app_number_info) | **GET** /v1/whatsapp/number-info | Get number status
[**get_whats_app_number_kyc_form**](WhatsAppPhoneNumbersApi.md#get_whats_app_number_kyc_form) | **GET** /v1/whatsapp/phone-numbers/kyc | Get KYC form spec
[**get_whats_app_number_remediation**](WhatsAppPhoneNumbersApi.md#get_whats_app_number_remediation) | **GET** /v1/whatsapp/phone-numbers/{id}/remediate | Get declined requirements
[**get_whats_app_phone_number**](WhatsAppPhoneNumbersApi.md#get_whats_app_phone_number) | **GET** /v1/whatsapp/phone-numbers/{phoneNumberId} | Get phone number
[**get_whats_app_phone_numbers**](WhatsAppPhoneNumbersApi.md#get_whats_app_phone_numbers) | **GET** /v1/whatsapp/phone-numbers | List phone numbers
[**list_whats_app_number_countries**](WhatsAppPhoneNumbersApi.md#list_whats_app_number_countries) | **GET** /v1/whatsapp/phone-numbers/countries | List offerable number countries
[**purchase_whats_app_phone_number**](WhatsAppPhoneNumbersApi.md#purchase_whats_app_phone_number) | **POST** /v1/whatsapp/phone-numbers/purchase | Purchase phone number
[**release_whats_app_phone_number**](WhatsAppPhoneNumbersApi.md#release_whats_app_phone_number) | **DELETE** /v1/whatsapp/phone-numbers/{phoneNumberId} | Release phone number
[**remediate_whats_app_number**](WhatsAppPhoneNumbersApi.md#remediate_whats_app_number) | **POST** /v1/whatsapp/phone-numbers/{id}/remediate | Resubmit a declined number
[**search_available_whats_app_numbers**](WhatsAppPhoneNumbersApi.md#search_available_whats_app_numbers) | **GET** /v1/whatsapp/phone-numbers/available | Search available numbers
[**submit_whats_app_number_kyc**](WhatsAppPhoneNumbersApi.md#submit_whats_app_number_kyc) | **POST** /v1/whatsapp/phone-numbers/kyc | Submit KYC
[**upload_whats_app_number_kyc_document**](WhatsAppPhoneNumbersApi.md#upload_whats_app_number_kyc_document) | **POST** /v1/whatsapp/phone-numbers/kyc/upload-document | Upload a KYC document
[**validate_whats_app_number_kyc_address**](WhatsAppPhoneNumbersApi.md#validate_whats_app_number_kyc_address) | **POST** /v1/whatsapp/phone-numbers/kyc/validate-address | Pre-validate KYC address



## check_whats_app_number_availability

> models::CheckPhoneNumberAvailability200Response check_whats_app_number_availability(country)
Check country availability

Deprecated alias of `/v1/phone-numbers/availability`; same contract. New integrations should use that path.  Pre-purchase check, so you can warn BEFORE a customer invests in KYC (regulated review is async, 1-3 days). Tells you whether we have deliverable inventory, and what address the customer needs:   - `addressConstraint: geo`  → the registered address MUST be in one of     the returned `areas` (the only place we have stock). A different-area     address passes pre-approval but the number can never be assigned.   - `addressConstraint: country` → any in-country address works.   - `addressConstraint: none` → field-only / instant country, no address. Call this before starting the KYC form for regulated countries. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**country** | **String** | ISO-2 country code. | [required] |

### Return type

[**models::CheckPhoneNumberAvailability200Response**](checkPhoneNumberAvailability_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_whats_app_number_kyc_link

> models::CreatePhoneNumberKycLink200Response create_whats_app_number_kyc_link(create_phone_number_kyc_link_request)
Create a hosted KYC link

Deprecated alias of `/v1/phone-numbers/kyc/share`; same contract. New integrations should use that path.  Create a single-use, 7-day hosted KYC link that your end customer completes WITHOUT a Zernio login — useful when the person who holds the ID and address is not your team. They fill the regulated verification on a Zernio-hosted page; the number provisions under YOUR account once they submit. Only regulated (KYC) countries are valid: a country that does not require KYC returns 400.  White-label the page with `branding` (your company name, logo, brand color). Supply `redirect_url` to send the end customer back to your own site after a successful submit (completion params are appended — see below). Listen for the `whatsapp.number.kyc_submitted` webhook to react when the form is completed. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_phone_number_kyc_link_request** | [**CreatePhoneNumberKycLinkRequest**](CreatePhoneNumberKycLinkRequest.md) |  | [required] |

### Return type

[**models::CreatePhoneNumberKycLink200Response**](createPhoneNumberKycLink_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


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
Get KYC form spec

Deprecated alias of `/v1/phone-numbers/kyc`; same contract. New integrations should use that path.  For a Tier 3/4 country, the fields the end customer must provide (Telnyx regulatory requirements) before a number can be ordered: text, date, address, or file (document) per requirement. 

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


## get_whats_app_number_remediation

> models::GetWhatsAppNumberRemediation200Response get_whats_app_number_remediation(id)
Get declined requirements

Deprecated alias of `/v1/phone-numbers/{id}/remediate`; same contract. New integrations should use that path.  For a number in `regulatory_declined`, returns ONLY the requirements the reviewer flagged declined, as a form spec (same shape as the KYC form GET). The customer fixes just those — Telnyx supports correcting a declined requirement group and re-submitting it (no new number/group). Falls back to the full spec if the provider exposes no per-requirement flags. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | WhatsAppPhoneNumber id. | [required] |

### Return type

[**models::GetWhatsAppNumberRemediation200Response**](getWhatsAppNumberRemediation_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_phone_number

> models::GetPhoneNumber200Response get_whats_app_phone_number(phone_number_id)
Get phone number

Deprecated alias of `/v1/phone-numbers/{id}`; same contract. New integrations should use that path.  Retrieve the current status of a purchased phone number. Poll this to track Meta pre-verification (US sync path) and, for regulated (Tier 3/4) numbers, the async lifecycle: pending_regulatory → active (or regulatory_declined). When a regulated number has an Onfido ID step, `onfidoVerificationUrl` appears here once the order is placed — forward it to the end user. (Or subscribe to the whatsapp.number.* webhooks instead of polling.) 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**phone_number_id** | **String** | Phone number record ID | [required] |

### Return type

[**models::GetPhoneNumber200Response**](getPhoneNumber_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_whats_app_phone_numbers

> models::ListPhoneNumbers200Response get_whats_app_phone_numbers(status, profile_id)
List phone numbers

Deprecated alias of `/v1/phone-numbers`; same contract. New integrations should use that path.  List all WhatsApp phone numbers purchased by the authenticated user. By default, released numbers are excluded. Connected (bring-your-own) numbers are returned in the separate `connected` array — they are not billed and have no provisioning lifecycle. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**status** | Option<**String**> | Filter by status (by default excludes released numbers). NOTE: `status=pending_regulatory` returns the \"provisioning\" view — numbers still in review PLUS recently-declined (last 30 days) ones, so a failed registration surfaces (with `regulatoryDeclineReason`) instead of silently disappearing. Declined numbers can be re-submitted via POST /v1/whatsapp/phone-numbers/{id}/remediate. `verifying` is the short-lived state after the number is provisioned on our side while WhatsApp confirms the activation code; the number is not billed until it reaches `active`.  |  |
**profile_id** | Option<**String**> | Filter by profile |  |

### Return type

[**models::ListPhoneNumbers200Response**](listPhoneNumbers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_whats_app_number_countries

> models::ListWhatsAppNumberCountries200Response list_whats_app_number_countries()
List offerable number countries

Deprecated alias of `/v1/phone-numbers/countries`; same contract. New integrations should use that path.  The WhatsApp number countries available to purchase, each with its flat monthly price (cents), regulatory tier, whether it needs end-user KYC (Tier 3/4), and whether outbound calling is available (not BIC-blocked). Drives the country picker. Tier-4 countries appear only when enabled. 

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

> models::PurchasePhoneNumber200Response purchase_whats_app_phone_number(purchase_whats_app_phone_number_request)
Purchase phone number

Deprecated alias of `/v1/phone-numbers/purchase`; same contract. New integrations should use that path.  Payment-first: you do not pick a specific number, the system provisions one and auto-assigns it. With usage-based billing active and a payment method on file, the number provisions inline and bills per month on your usage-based invoice (there is no checkout redirect). No payment method on file returns `402 PAYMENT_REQUIRED`; a regulated country returns `202` with `status: \"kyc_required\"` and a `kycUrl`.  Requires usage-based billing (the Usage plan). The maximum number of phone numbers is determined by the user's plan. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**purchase_whats_app_phone_number_request** | [**PurchaseWhatsAppPhoneNumberRequest**](PurchaseWhatsAppPhoneNumberRequest.md) |  | [required] |

### Return type

[**models::PurchasePhoneNumber200Response**](purchasePhoneNumber_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## release_whats_app_phone_number

> models::ReleasePhoneNumber200Response release_whats_app_phone_number(phone_number_id)
Release phone number

Deprecated alias of `/v1/phone-numbers/{id}`; same contract. New integrations should use that path.  Release a purchased phone number. This will: 1. Disconnect any linked WhatsApp social account 2. Decrement the Stripe subscription quantity (or cancel if last number) 3. Release the number from Telnyx 4. Mark the number as released 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**phone_number_id** | **String** | Phone number record ID | [required] |

### Return type

[**models::ReleasePhoneNumber200Response**](releasePhoneNumber_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remediate_whats_app_number

> models::RemediatePhoneNumber200Response remediate_whats_app_number(id, remediate_phone_number_request)
Resubmit a declined number

Deprecated alias of `/v1/phone-numbers/{id}/remediate`; same contract. New integrations should use that path.  Submit corrected values/documents for the declined requirement(s). We PATCH them onto the SAME requirement group and re-submit it for approval; the number goes `regulatory_declined` → `pending_regulatory`. No new number and no new billing. Body shape matches the KYC submit (values / documents / address) — send only the corrected fields. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**remediate_phone_number_request** | [**RemediatePhoneNumberRequest**](RemediatePhoneNumberRequest.md) |  | [required] |

### Return type

[**models::RemediatePhoneNumber200Response**](remediatePhoneNumber_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_available_whats_app_numbers

> models::SearchAvailableWhatsAppNumbers200Response search_available_whats_app_numbers(country, r#type, prefix, locality, contains, limit)
Search available numbers

Deprecated alias of `/v1/phone-numbers/available`; same contract. New integrations should use that path.  Search the provider's inventory for numbers available to purchase in a country (default US). Optional filters narrow the results. The country must be offerable (see GET /v1/whatsapp/phone-numbers/countries). 

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

> models::SubmitPhoneNumberKyc200Response submit_whats_app_number_kyc(submit_whats_app_number_kyc_request)
Submit KYC

Deprecated alias of `/v1/phone-numbers/kyc`; same contract. New integrations should use that path.  Submit the end customer's KYC (textual values, uploaded documents, address) for a Tier 3/4 country. Documents are streamed straight to the number provider and are not stored by Zernio. Builds + submits a regulatory requirement group and claims a pending_regulatory slot; the number is ordered + activated once the provider approves (asynchronous). A customer may hold several same-country numbers in review at once; a double-submit of the SAME attempt is deduped via `submissionId`.  For an ID-card document requirement, carriers commonly require BOTH sides: combine the front and back into a single file before uploading (the dashboard does this automatically). A one-sided ID is a common decline reason; fix it via POST /v1/whatsapp/phone-numbers/{id}/remediate.  Before submitting, call GET /v1/whatsapp/phone-numbers/availability to check the country has deliverable inventory and, for geographic-match countries, which area the address must be in — otherwise the submission can pass review yet never be assignable a number. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**submit_whats_app_number_kyc_request** | [**SubmitWhatsAppNumberKycRequest**](SubmitWhatsAppNumberKycRequest.md) |  | [required] |

### Return type

[**models::SubmitPhoneNumberKyc200Response**](submitPhoneNumberKyc_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upload_whats_app_number_kyc_document

> models::UploadPhoneNumberKycDocument200Response upload_whats_app_number_kyc_document(x_filename, body)
Upload a KYC document

Deprecated alias of `/v1/phone-numbers/kyc/upload-document`; same contract. New integrations should use that path.  Upload ONE document and get back its provider document id, to reference from POST /v1/whatsapp/phone-numbers/kyc via `documents[].documentId`. Send the RAW file bytes as the request body (not base64); put the filename in the `X-Filename` header. Uploading documents one-per-request keeps each request under the ~4.5MB body limit. The document streams straight to the number provider and is not stored by Zernio. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**x_filename** | **String** | URL-encoded original filename. | [required] |
**body** | **std::path::PathBuf** |  | [required] |

### Return type

[**models::UploadPhoneNumberKycDocument200Response**](uploadPhoneNumberKycDocument_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/octet-stream
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## validate_whats_app_number_kyc_address

> models::ValidatePhoneNumberKycAddress200Response validate_whats_app_number_kyc_address(validate_phone_number_kyc_address_request)
Pre-validate KYC address

Deprecated alias of `/v1/phone-numbers/kyc/validate-address`; same contract. New integrations should use that path.  Optional early check for the address step of a Tier 4 (end-user identity) registration: validates a postal address for deliverability BEFORE the full KYC submit, so it can be corrected before any documents are uploaded. The full submit (POST /v1/whatsapp/phone-numbers/kyc) re-validates the address, so this call is purely a fast feedback path and skipping it is safe. Only the postal address is sent (no documents, no gov-ID fields). A region (`administrative_area`) is required by the validator; when it is omitted the pre-check is skipped and `{ ok: true, skipped: true }` is returned (the final submit still validates). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**validate_phone_number_kyc_address_request** | [**ValidatePhoneNumberKycAddressRequest**](ValidatePhoneNumberKycAddressRequest.md) |  | [required] |

### Return type

[**models::ValidatePhoneNumberKycAddress200Response**](validatePhoneNumberKycAddress_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

