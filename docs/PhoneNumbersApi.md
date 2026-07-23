# \PhoneNumbersApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancel_phone_number_port_in**](PhoneNumbersApi.md#cancel_phone_number_port_in) | **DELETE** /v1/phone-numbers/port-in/{id} | Cancel a port-in
[**check_phone_number_availability**](PhoneNumbersApi.md#check_phone_number_availability) | **GET** /v1/phone-numbers/availability | Check country availability
[**check_phone_number_portability**](PhoneNumbersApi.md#check_phone_number_portability) | **POST** /v1/phone-numbers/port-in/check | Check portability
[**create_phone_number_kyc_link**](PhoneNumbersApi.md#create_phone_number_kyc_link) | **POST** /v1/phone-numbers/kyc/share | Create a hosted KYC link
[**create_phone_number_port_in**](PhoneNumbersApi.md#create_phone_number_port_in) | **POST** /v1/phone-numbers/port-in | Port numbers in
[**get_phone_number**](PhoneNumbersApi.md#get_phone_number) | **GET** /v1/phone-numbers/{id} | Get phone number
[**get_phone_number_kyc_form**](PhoneNumbersApi.md#get_phone_number_kyc_form) | **GET** /v1/phone-numbers/kyc | Get KYC form spec
[**get_phone_number_port_in_order_requirements**](PhoneNumbersApi.md#get_phone_number_port_in_order_requirements) | **GET** /v1/phone-numbers/port-in/{id}/requirements | A port-in order's pending requirements
[**get_phone_number_port_in_requirements**](PhoneNumbersApi.md#get_phone_number_port_in_requirements) | **GET** /v1/phone-numbers/port-in/requirements | Country porting requirements
[**get_phone_number_remediation**](PhoneNumbersApi.md#get_phone_number_remediation) | **GET** /v1/phone-numbers/{id}/remediate | Get declined requirements
[**list_phone_number_countries**](PhoneNumbersApi.md#list_phone_number_countries) | **GET** /v1/phone-numbers/countries | List offerable number countries
[**list_phone_number_port_ins**](PhoneNumbersApi.md#list_phone_number_port_ins) | **GET** /v1/phone-numbers/port-in | List port-in orders
[**list_phone_numbers**](PhoneNumbersApi.md#list_phone_numbers) | **GET** /v1/phone-numbers | List phone numbers
[**purchase_phone_number**](PhoneNumbersApi.md#purchase_phone_number) | **POST** /v1/phone-numbers/purchase | Purchase phone number
[**release_phone_number**](PhoneNumbersApi.md#release_phone_number) | **DELETE** /v1/phone-numbers/{id} | Release phone number
[**remediate_phone_number**](PhoneNumbersApi.md#remediate_phone_number) | **POST** /v1/phone-numbers/{id}/remediate | Resubmit a declined number
[**review_phone_number_kyc_packet**](PhoneNumbersApi.md#review_phone_number_kyc_packet) | **POST** /v1/phone-numbers/kyc/review-packet | Pre-review a KYC packet
[**search_available_phone_numbers**](PhoneNumbersApi.md#search_available_phone_numbers) | **GET** /v1/phone-numbers/available | Search available numbers
[**submit_phone_number_kyc**](PhoneNumbersApi.md#submit_phone_number_kyc) | **POST** /v1/phone-numbers/kyc | Submit KYC
[**upload_phone_number_kyc_document**](PhoneNumbersApi.md#upload_phone_number_kyc_document) | **POST** /v1/phone-numbers/kyc/upload-document | Upload a KYC document
[**upload_phone_number_port_in_document**](PhoneNumbersApi.md#upload_phone_number_port_in_document) | **POST** /v1/phone-numbers/port-in/documents | Upload a porting document
[**validate_phone_number_kyc_address**](PhoneNumbersApi.md#validate_phone_number_kyc_address) | **POST** /v1/phone-numbers/kyc/validate-address | Pre-validate KYC address
[**view_phone_number_kyc_document**](PhoneNumbersApi.md#view_phone_number_kyc_document) | **GET** /v1/phone-numbers/kyc/document/{documentId} | View a KYC document on file



## cancel_phone_number_port_in

> models::CancelPhoneNumberPortIn200Response cancel_phone_number_port_in(id)
Cancel a port-in

Cancel an in-flight port (wrong number, staying with the old carrier). Only orders that haven't ported can be cancelled; a completed port is a normal number release instead. The carrier may report `cancel-pending` briefly while the losing carrier acknowledges; it settles to `cancelled`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Porting order ID (from the port-in list). | [required] |

### Return type

[**models::CancelPhoneNumberPortIn200Response**](cancelPhoneNumberPortIn_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## check_phone_number_availability

> models::CheckPhoneNumberAvailability200Response check_phone_number_availability(country, number_type)
Check country availability

Pre-purchase check, so you can warn BEFORE a customer invests in KYC (regulated review is async, 1-3 days). Tells you whether we have deliverable inventory, and what address the customer needs:   - `addressConstraint: geo`  → the registered address MUST be in one of     the returned `areas` (the only place we have stock). A different-area     address passes pre-approval but the number can never be assigned.   - `addressConstraint: country` → any in-country address works.   - `addressConstraint: none` → field-only / instant country, no address. Call this before starting the KYC form for regulated countries. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**country** | **String** | ISO-2 country code. | [required] |
**number_type** | Option<**String**> | Check a specific offered type (stock and address constraints are per type). Omitted = the country's default type. |  |

### Return type

[**models::CheckPhoneNumberAvailability200Response**](checkPhoneNumberAvailability_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## check_phone_number_portability

> models::CheckPhoneNumberPortability200Response check_phone_number_portability(check_phone_number_portability_request)
Check portability

Pre-flight portability check: whether each number can be ported in and whether it qualifies for FastPort, BEFORE the user commits to a port order (LOA, invoice, service address). Read-only; creates no order and bills nothing. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**check_phone_number_portability_request** | [**CheckPhoneNumberPortabilityRequest**](CheckPhoneNumberPortabilityRequest.md) |  | [required] |

### Return type

[**models::CheckPhoneNumberPortability200Response**](checkPhoneNumberPortability_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_phone_number_kyc_link

> models::CreatePhoneNumberKycLink200Response create_phone_number_kyc_link(create_phone_number_kyc_link_request)
Create a hosted KYC link

Create a single-use, 7-day hosted KYC link that your end customer completes WITHOUT a Zernio login — useful when the person who holds the ID and address is not your team. They fill the regulated verification on a Zernio-hosted page; the number provisions under YOUR account once they submit. Only regulated (KYC) countries are valid: a country that does not require KYC returns 400.  White-label the page with `branding` (your company name, logo, brand color). Supply `redirect_url` to send the end customer back to your own site after a successful submit (completion params are appended — see below). Listen for the `whatsapp.number.kyc_submitted` webhook to react when the form is completed. 

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


## create_phone_number_port_in

> models::CreatePhoneNumberPortIn201Response create_phone_number_port_in(create_phone_number_port_in_request)
Port numbers in

Submit a port-in for one or more existing numbers from another carrier. Creates the carrier order(s), attaches the end-user (current account) info plus the LOA and invoice documents, and submits to the losing carrier. The transfer PIN is forwarded to the carrier and never stored. Ported numbers arrive voice-ready (and SMS-ready where the order supports messaging).  Run the portability check (POST /v1/phone-numbers/port-in/check) and upload the two documents (POST /v1/phone-numbers/port-in/documents) first — uploaded documents must be attached to an order within 30 minutes or the carrier deletes them, so upload right before this call. The carrier may split the numbers into several orders (by country, number type, losing carrier); `orders` carries per-order results, and a partial failure still returns 201 with the failed orders' `error` set (they stay as cancellable drafts).  Non-US/CA numbers additionally need the country-specific values from GET /v1/phone-numbers/port-in/requirements, passed via `requirements`, and must be submitted one country per request. When required information is still missing after submission, the order is kept as a resumable draft whose `error` / `declineReason` names the gaps. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_phone_number_port_in_request** | [**CreatePhoneNumberPortInRequest**](CreatePhoneNumberPortInRequest.md) |  | [required] |

### Return type

[**models::CreatePhoneNumberPortIn201Response**](createPhoneNumberPortIn_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_phone_number

> models::GetPhoneNumber200Response get_phone_number(id)
Get phone number

Retrieve the current status of a purchased phone number. Poll this to track Meta pre-verification (US sync path) and, for regulated (Tier 3/4) numbers, the async lifecycle: pending_regulatory → active (or regulatory_declined). When a regulated number has an Onfido ID step, `onfidoVerificationUrl` appears here once the order is placed — forward it to the end user. (Or subscribe to the whatsapp.number.* webhooks instead of polling.) 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Phone number record ID | [required] |

### Return type

[**models::GetPhoneNumber200Response**](getPhoneNumber_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_phone_number_kyc_form

> models::GetPhoneNumberKycForm200Response get_phone_number_kyc_form(country, number_type)
Get KYC form spec

For a Tier 3/4 country, the fields the end customer must provide (Telnyx regulatory requirements) before a number can be ordered: text, date, address, or file (document) per requirement. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**country** | **String** |  | [required] |
**number_type** | Option<**String**> | Requirements and reuse eligibility are per (country, type). Omitted = the country's default type. Pass the same value on the POST. |  |

### Return type

[**models::GetPhoneNumberKycForm200Response**](getPhoneNumberKycForm_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_phone_number_port_in_order_requirements

> models::GetPhoneNumberPortInOrderRequirements200Response get_phone_number_port_in_order_requirements(id)
A port-in order's pending requirements

The live requirements on an EXISTING porting order: which are filled, which are still pending, and which bounced on review (`requirement-info-exception`). Use it to fix and resubmit a rejected international port. Same field shape as the country-level requirements endpoint, plus per-requirement status. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Porting order ID (from the port-in list). | [required] |

### Return type

[**models::GetPhoneNumberPortInOrderRequirements200Response**](getPhoneNumberPortInOrderRequirements_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_phone_number_port_in_requirements

> models::GetPhoneNumberPortInRequirements200Response get_phone_number_port_in_requirements(country, number_type)
Country porting requirements

The country-specific information a port-in needs BEYOND the LOA, invoice, and account/address details — e.g. an ID copy, proof of address, a tax id, or a porting code. Call it after the portability check (which returns each number's `countryCode` and `phoneNumberType`), render the fields, and pass the collected values as the create request's `requirements`. US/CA return an empty list. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**country** | **String** | ISO country of the numbers being ported (a supported port-in country). | [required] |
**number_type** | Option<**String**> | The portability check's phoneNumberType — requirements differ by type. |  |[default to local]

### Return type

[**models::GetPhoneNumberPortInRequirements200Response**](getPhoneNumberPortInRequirements_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_phone_number_remediation

> models::GetPhoneNumberRemediation200Response get_phone_number_remediation(id)
Get declined requirements

For a number in `regulatory_declined`, returns ONLY the requirements the reviewer flagged declined, as a form spec (same shape as the KYC form GET). The customer fixes just those — Telnyx supports correcting a declined requirement group and re-submitting it (no new number/group). Falls back to the full spec if the provider exposes no per-requirement flags. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Phone number record ID. | [required] |

### Return type

[**models::GetPhoneNumberRemediation200Response**](getPhoneNumberRemediation_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_phone_number_countries

> models::ListPhoneNumberCountries200Response list_phone_number_countries()
List offerable number countries

The phone number countries available to purchase, each with its flat monthly price (cents), regulatory tier, whether it needs end-user KYC (Tier 3/4), and per-feature availability (PSTN calls, WhatsApp, SMS, and WhatsApp Business Calling outbound). Drives the country picker. Tier-4 countries appear only when enabled. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListPhoneNumberCountries200Response**](listPhoneNumberCountries_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_phone_number_port_ins

> models::ListPhoneNumberPortIns200Response list_phone_number_port_ins()
List port-in orders

Your porting orders, newest first (max 50). Poll this for port progress: pending, confirmed FOC date, exception reason, or ported. 

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListPhoneNumberPortIns200Response**](listPhoneNumberPortIns_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_phone_numbers

> models::ListPhoneNumbers200Response list_phone_numbers(status, profile_id)
List phone numbers

List all phone numbers purchased by the authenticated user. By default, released numbers are excluded. Connected (bring-your-own) WhatsApp numbers are returned in the separate `connected` array; they are not billed and have no provisioning lifecycle. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**status** | Option<**String**> | Filter by status (by default excludes released numbers). NOTE: `status=pending_regulatory` returns the \"provisioning\" view — numbers still in review PLUS recently-declined (last 30 days) ones, so a failed registration surfaces (with `regulatoryDeclineReason`) instead of silently disappearing. Declined numbers can be re-submitted via POST /v1/phone-numbers/{id}/remediate. `verifying` is the short-lived state after the number is provisioned on our side while WhatsApp confirms the activation code; the number is not billed until it reaches `active`.  |  |
**profile_id** | Option<**String**> | Filter by profile |  |

### Return type

[**models::ListPhoneNumbers200Response**](listPhoneNumbers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## purchase_phone_number

> models::PurchasePhoneNumber200Response purchase_phone_number(purchase_phone_number_request)
Purchase phone number

Payment-first: you do not pick a specific number, the system provisions one and auto-assigns it. With usage-based billing active and a payment method on file, the number provisions inline and bills per month on your usage-based invoice (there is no checkout redirect). No payment method on file returns `402 PAYMENT_REQUIRED`; a regulated country returns `202` with `status: \"kyc_required\"` and a `kycUrl`.  Requires usage-based billing (the Usage plan). The maximum number of phone numbers is determined by the user's plan. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**purchase_phone_number_request** | [**PurchasePhoneNumberRequest**](PurchasePhoneNumberRequest.md) |  | [required] |

### Return type

[**models::PurchasePhoneNumber200Response**](purchasePhoneNumber_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## release_phone_number

> models::ReleasePhoneNumber200Response release_phone_number(id)
Release phone number

Release a purchased phone number. This will: 1. Disconnect any linked WhatsApp social account 2. Decrement the Stripe subscription quantity (or cancel if last number) 3. Release the number from Telnyx 4. Mark the number as released 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Phone number record ID | [required] |

### Return type

[**models::ReleasePhoneNumber200Response**](releasePhoneNumber_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remediate_phone_number

> models::RemediatePhoneNumber200Response remediate_phone_number(id, remediate_phone_number_request)
Resubmit a declined number

Submit corrected values/documents for the declined requirement(s). We PATCH them onto the SAME requirement group and re-submit it for approval; the number goes `regulatory_declined` → `pending_regulatory`. No new number and no new billing. Body shape matches the KYC submit (values / documents / address) — send only the corrected fields. 

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


## review_phone_number_kyc_packet

> models::ReviewPhoneNumberKycPacket200Response review_phone_number_kyc_packet(review_phone_number_kyc_packet_request)
Pre-review a KYC packet

Advisory dry-run of a regulated-KYC packet before submitting: reviews the exact documents the regulator will see (referenced by the ids from POST /v1/phone-numbers/kyc/upload-document) against the declared values and address, and returns plain-language advisories for likely decline reasons (wrong document type, mismatched address, one-sided ID scans). Non-blocking: advisories are warnings, submitting anyway is always allowed, and any review failure degrades to an empty list. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**review_phone_number_kyc_packet_request** | [**ReviewPhoneNumberKycPacketRequest**](ReviewPhoneNumberKycPacketRequest.md) |  | [required] |

### Return type

[**models::ReviewPhoneNumberKycPacket200Response**](reviewPhoneNumberKycPacket_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_available_phone_numbers

> models::SearchAvailablePhoneNumbers200Response search_available_phone_numbers(country, r#type, prefix, locality, contains, sms, limit)
Search available numbers

Search the provider's inventory for numbers available to purchase in a country (default US). Optional filters narrow the results. The country must be offerable (see GET /v1/phone-numbers/countries). Voice capability is always required; pass `sms=true` to only see numbers that can also text (SMS support is per-number, not per-country). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**country** | Option<**String**> |  |  |[default to US]
**r#type** | Option<**String**> | Number type; defaults to the country's WhatsApp-safe type |  |
**prefix** | Option<**String**> | Area code |  |
**locality** | Option<**String**> | City |  |
**contains** | Option<**String**> | Pattern to match within the number |  |
**sms** | Option<**bool**> | true narrows the pool to SMS-capable numbers. Each result still carries its full `features` list for per-number capability badging. |  |
**limit** | Option<**i32**> |  |  |[default to 20]

### Return type

[**models::SearchAvailablePhoneNumbers200Response**](searchAvailablePhoneNumbers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## submit_phone_number_kyc

> models::SubmitPhoneNumberKyc200Response submit_phone_number_kyc(submit_phone_number_kyc_request)
Submit KYC

Submit the end customer's KYC (textual values, uploaded documents, address) for a Tier 3/4 country. Documents are streamed straight to the number provider and are not stored by Zernio. Builds + submits a regulatory requirement group and claims a pending_regulatory slot; the number is ordered + activated once the provider approves (asynchronous). A customer may hold several same-country numbers in review at once; a double-submit of the SAME attempt is deduped via `submissionId`.  For an ID-card document requirement, carriers commonly require BOTH sides: combine the front and back into a single file before uploading (the dashboard does this automatically). A one-sided ID is a common decline reason; fix it via POST /v1/phone-numbers/{id}/remediate.  Before submitting, call GET /v1/phone-numbers/availability to check the country has deliverable inventory and, for geographic-match countries, which area the address must be in — otherwise the submission can pass review yet never be assignable a number. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**submit_phone_number_kyc_request** | [**SubmitPhoneNumberKycRequest**](SubmitPhoneNumberKycRequest.md) |  | [required] |

### Return type

[**models::SubmitPhoneNumberKyc200Response**](submitPhoneNumberKyc_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upload_phone_number_kyc_document

> models::UploadPhoneNumberKycDocument200Response upload_phone_number_kyc_document(x_filename, body)
Upload a KYC document

Upload ONE document and get back its provider document id, to reference from POST /v1/phone-numbers/kyc via `documents[].documentId`. Send the RAW file bytes as the request body (not base64); put the filename in the `X-Filename` header. Uploading documents one-per-request keeps each request under the ~4.5MB body limit. The document streams straight to the number provider and is not stored by Zernio. 

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


## upload_phone_number_port_in_document

> models::UploadPhoneNumberPortInDocument200Response upload_phone_number_port_in_document(file, kind)
Upload a porting document

Upload ONE porting document and get back its `documentId`. For the signed LOA / carrier invoice the id goes to `loaDocumentId` / `invoiceDocumentId`; for a country-specific document requirement (international ports) it becomes that requirement's `fieldValue`. Requirement documents are normalized to PDF automatically (regulators reject raw images). PDF, JPEG, or PNG, 10MB max. Uploads must be attached to an order within 30 minutes or the carrier deletes them. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**file** | **std::path::PathBuf** | The document (PDF/JPEG/PNG, 10MB max). | [required] |
**kind** | Option<**String**> | 'loa', 'invoice', or any short slug for requirement documents. Informational; used for the stored filename. |  |

### Return type

[**models::UploadPhoneNumberPortInDocument200Response**](uploadPhoneNumberPortInDocument_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## validate_phone_number_kyc_address

> models::ValidatePhoneNumberKycAddress200Response validate_phone_number_kyc_address(validate_phone_number_kyc_address_request)
Pre-validate KYC address

Optional early check for the address step of a Tier 4 (end-user identity) registration: validates a postal address for deliverability BEFORE the full KYC submit, so it can be corrected before any documents are uploaded. The full submit (POST /v1/phone-numbers/kyc) re-validates the address, so this call is purely a fast feedback path and skipping it is safe. Only the postal address is sent (no documents, no gov-ID fields). A region (`administrative_area`) is required by the validator; when it is omitted the pre-check is skipped and `{ ok: true, skipped: true }` is returned (the final submit still validates). 

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


## view_phone_number_kyc_document

> std::path::PathBuf view_phone_number_kyc_document(document_id)
View a KYC document on file

Stream a document backing a reusable verification (the `documentId` values from GET /v1/phone-numbers/kyc `reusable.options[].details[]`), so the account holder can see what's on file before reusing it. Returned inline as `application/pdf` (uploads are normalized to PDF). Auth-scoped: a document is viewable only when its id is referenced by one of the caller's own numbers — otherwise `404`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**document_id** | **String** | The Telnyx document id (from `reusable.options[].details[].documentId`). | [required] |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/pdf, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

