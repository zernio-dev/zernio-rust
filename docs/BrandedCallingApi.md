# \BrandedCallingApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**attach_branded_calling_numbers**](BrandedCallingApi.md#attach_branded_calling_numbers) | **POST** /v1/branded-calling/identities/{id}/numbers | Attach numbers to a verified identity
[**confirm_branded_calling_authorizer_email**](BrandedCallingApi.md#confirm_branded_calling_authorizer_email) | **POST** /v1/branded-calling/identities/{id}/verify-email/confirm | Confirm the authorizer's code
[**create_branded_calling_enterprise**](BrandedCallingApi.md#create_branded_calling_enterprise) | **POST** /v1/branded-calling/enterprises | Register a business for Branded Calling
[**create_branded_calling_identity**](BrandedCallingApi.md#create_branded_calling_identity) | **POST** /v1/branded-calling/identities | Create a caller identity
[**delete_branded_calling_enterprise**](BrandedCallingApi.md#delete_branded_calling_enterprise) | **DELETE** /v1/branded-calling/enterprises/{id} | Delete a registered business
[**delete_branded_calling_identity**](BrandedCallingApi.md#delete_branded_calling_identity) | **DELETE** /v1/branded-calling/identities/{id} | Delete a caller identity
[**detach_branded_calling_numbers**](BrandedCallingApi.md#detach_branded_calling_numbers) | **DELETE** /v1/branded-calling/identities/{id}/numbers | Detach numbers from an identity
[**get_branded_calling_enterprise**](BrandedCallingApi.md#get_branded_calling_enterprise) | **GET** /v1/branded-calling/enterprises/{id} | Get a registered business
[**get_branded_calling_identity**](BrandedCallingApi.md#get_branded_calling_identity) | **GET** /v1/branded-calling/identities/{id} | Get a caller identity
[**list_branded_calling_call_reasons**](BrandedCallingApi.md#list_branded_calling_call_reasons) | **GET** /v1/branded-calling/call-reasons | List pre-approved call reasons
[**list_branded_calling_enterprises**](BrandedCallingApi.md#list_branded_calling_enterprises) | **GET** /v1/branded-calling/enterprises | List registered businesses
[**list_branded_calling_identities**](BrandedCallingApi.md#list_branded_calling_identities) | **GET** /v1/branded-calling/identities | List caller identities
[**list_branded_calling_identity_numbers**](BrandedCallingApi.md#list_branded_calling_identity_numbers) | **GET** /v1/branded-calling/identities/{id}/numbers | List the numbers on a caller identity
[**preflight_branded_calling_identity**](BrandedCallingApi.md#preflight_branded_calling_identity) | **POST** /v1/branded-calling/identities/preflight | Dry-run a caller identity before creating it
[**resend_branded_calling_authorizer_code**](BrandedCallingApi.md#resend_branded_calling_authorizer_code) | **POST** /v1/branded-calling/identities/{id}/verify-email | Resend the authorizer's code
[**share_branded_calling_identity_form**](BrandedCallingApi.md#share_branded_calling_identity_form) | **POST** /v1/branded-calling/share | Create a caller identity share link
[**update_branded_calling_identity**](BrandedCallingApi.md#update_branded_calling_identity) | **PATCH** /v1/branded-calling/identities/{id} | Edit or resubmit a caller identity



## attach_branded_calling_numbers

> models::ListBrandedCallingIdentityNumbers200Response attach_branded_calling_numbers(id, attach_branded_calling_numbers_request)
Attach numbers to a verified identity

Files a Letter of Authorization signed by you (Zernio is named as the authorized agent managing the numbers) and opens a vetting batch of up to 15 US numbers you own. The batch is all-or-nothing: one ineligible number refuses the whole call. Each number shows the identity once its own status reaches `verified`. A number belongs to one identity at a time. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**attach_branded_calling_numbers_request** | [**AttachBrandedCallingNumbersRequest**](AttachBrandedCallingNumbersRequest.md) |  | [required] |

### Return type

[**models::ListBrandedCallingIdentityNumbers200Response**](listBrandedCallingIdentityNumbers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## confirm_branded_calling_authorizer_email

> models::BrandedCallingIdentity confirm_branded_calling_authorizer_email(id, confirm_branded_calling_authorizer_email_request)
Confirm the authorizer's code

The last customer step. On success the stored references are filed and the identity is submitted to carrier vetting in the same call (`in_review`). If a later step fails the identity stays `pending_email_verification` with the email already verified; calling again resumes from that step. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**confirm_branded_calling_authorizer_email_request** | [**ConfirmBrandedCallingAuthorizerEmailRequest**](ConfirmBrandedCallingAuthorizerEmailRequest.md) |  | [required] |

### Return type

[**models::BrandedCallingIdentity**](BrandedCallingIdentity.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_branded_calling_enterprise

> models::BrandedCallingEnterprise create_branded_calling_enterprise(create_branded_calling_enterprise_request, idempotency_key)
Register a business for Branded Calling

Stores the legal entity behind your caller identities. Nothing is filed with the carrier until the business's first identity passes review. Only businesses registered in the US or Canada qualify (a FEIN or Canadian equivalent is required); any other country returns `422`. Send an `Idempotency-Key` so a retry replays the original response instead of registering the business twice. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_branded_calling_enterprise_request** | [**CreateBrandedCallingEnterpriseRequest**](CreateBrandedCallingEnterpriseRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. |  |

### Return type

[**models::BrandedCallingEnterprise**](BrandedCallingEnterprise.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_branded_calling_identity

> models::BrandedCallingIdentity create_branded_calling_identity(create_branded_calling_identity_request, idempotency_key)
Create a caller identity

A caller identity is what the callee sees: display name, logo and call reasons, backed by a registered business and three references the carrier vetting team phones. It starts in Zernio review (`requested`). Once approved, the carrier emails the authorizer a 6-digit code; confirm it with the verify-email endpoint and the identity goes into carrier vetting on its own. Track it with `GET` or the `branded_calling.identity.status_updated` webhook.  Billing: $100 per identity per month while it is verified. The first month is charged when the carrier verifies the identity, never when it is filed: nothing is charged while it is in our review or carrier vetting, or if it is rejected. An edit that sends a verified identity back to vetting pauses the fee until it is verified again. Branded calls add $0.10 each, counted on every outbound call from a verified branded number to a US destination (whether or not the callee's carrier displayed the branding); the surcharge shows as `brandedCallUSD` on the call's billing and in `GET /v1/voice/calls/estimate` when you pass `from`.  Run `POST /v1/branded-calling/identities/preflight` with the same body first to catch what the review would bounce. Send an `Idempotency-Key` so a retry replays the original response instead of creating a second identity. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_branded_calling_identity_request** | [**CreateBrandedCallingIdentityRequest**](CreateBrandedCallingIdentityRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. |  |

### Return type

[**models::BrandedCallingIdentity**](BrandedCallingIdentity.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_branded_calling_enterprise

> models::DeleteBrandedCallingEnterprise200Response delete_branded_calling_enterprise(id)
Delete a registered business

Refused while the business still has caller identities (delete those first).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::DeleteBrandedCallingEnterprise200Response**](deleteBrandedCallingEnterprise_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_branded_calling_identity

> models::DeleteBrandedCallingEnterprise200Response delete_branded_calling_identity(id)
Delete a caller identity

Detaches its numbers and removes the identity at the carrier, which ends the monthly fee. Refused while an infringement claim is open.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::DeleteBrandedCallingEnterprise200Response**](deleteBrandedCallingEnterprise_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## detach_branded_calling_numbers

> models::DetachBrandedCallingNumbers200Response detach_branded_calling_numbers(id, detach_branded_calling_numbers_request)
Detach numbers from an identity

Deregisters the numbers at the carrier and frees them for another identity. Up to 100 per call.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**detach_branded_calling_numbers_request** | [**DetachBrandedCallingNumbersRequest**](DetachBrandedCallingNumbersRequest.md) |  | [required] |

### Return type

[**models::DetachBrandedCallingNumbers200Response**](detachBrandedCallingNumbers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_branded_calling_enterprise

> models::BrandedCallingEnterprise get_branded_calling_enterprise(id)
Get a registered business

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::BrandedCallingEnterprise**](BrandedCallingEnterprise.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_branded_calling_identity

> models::BrandedCallingIdentity get_branded_calling_identity(id)
Get a caller identity

Poll this for review and vetting progress, or subscribe to `branded_calling.identity.status_updated`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::BrandedCallingIdentity**](BrandedCallingIdentity.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_branded_calling_call_reasons

> models::ListBrandedCallingCallReasons200Response list_branded_calling_call_reasons()
List pre-approved call reasons

The carrier catalogue of call reasons that pass vetting automatically. Any other wording is allowed on an identity but is vetted by hand.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListBrandedCallingCallReasons200Response**](listBrandedCallingCallReasons_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_branded_calling_enterprises

> models::ListBrandedCallingEnterprises200Response list_branded_calling_enterprises()
List registered businesses

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListBrandedCallingEnterprises200Response**](listBrandedCallingEnterprises_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_branded_calling_identities

> models::ListBrandedCallingIdentities200Response list_branded_calling_identities()
List caller identities

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListBrandedCallingIdentities200Response**](listBrandedCallingIdentities_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_branded_calling_identity_numbers

> models::ListBrandedCallingIdentityNumbers200Response list_branded_calling_identity_numbers(id)
List the numbers on a caller identity

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::ListBrandedCallingIdentityNumbers200Response**](listBrandedCallingIdentityNumbers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## preflight_branded_calling_identity

> models::PreflightBrandedCallingIdentity200Response preflight_branded_calling_identity(preflight_branded_calling_identity_request)
Dry-run a caller identity before creating it

Validates the exact body `POST /v1/branded-calling/identities` takes and runs the same deterministic lints the review runs on it without creating anything, with the same codes and fields the queued identity's findings carry. A `block` finding is what the review would bounce (two references sharing a phone, a reference inside the business, an invalid timezone); a `warn` finding slows vetting (a display name that does not read as the business, a call reason outside the carrier catalogue, a public-mailbox authorizer, a logo that does not answer). `ok` is true when there is no `block`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**preflight_branded_calling_identity_request** | [**PreflightBrandedCallingIdentityRequest**](PreflightBrandedCallingIdentityRequest.md) |  | [required] |

### Return type

[**models::PreflightBrandedCallingIdentity200Response**](preflightBrandedCallingIdentity_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## resend_branded_calling_authorizer_code

> models::ResendBrandedCallingAuthorizerCode200Response resend_branded_calling_authorizer_code(id)
Resend the authorizer's code

Emails the authorizer a fresh 6-digit code (the previous one stops working). Only while the identity is `pending_email_verification`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::ResendBrandedCallingAuthorizerCode200Response**](resendBrandedCallingAuthorizerCode_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## share_branded_calling_identity_form

> models::ShareBrandedCallingIdentityForm200Response share_branded_calling_identity_form(share_branded_calling_identity_form_request)
Create a caller identity share link

Creates a single-use link (valid 7 days) where the end business fills in the caller identity itself, with no Zernio login: display name, logo, call reasons, the authorizer and the three references. What it submits lands under your team as `requested`, the same review as an API submission, and `branded_calling.identity.status_updated` fires. Scope the link with `identityId` (complete an identity that is `requested` or `changes_requested`), with `enterpriseId` (a new identity for a registered business), or with neither (the business registers itself and its first identity). The person opening the link can forward a fresh one to someone else, which retires theirs. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**share_branded_calling_identity_form_request** | Option<[**ShareBrandedCallingIdentityFormRequest**](ShareBrandedCallingIdentityFormRequest.md)> |  |  |

### Return type

[**models::ShareBrandedCallingIdentityForm200Response**](shareBrandedCallingIdentityForm_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_branded_calling_identity

> models::BrandedCallingIdentity update_branded_calling_identity(id, update_branded_calling_identity_request)
Edit or resubmit a caller identity

Allowed while the identity is `requested`, `changes_requested` or `rejected`. Answering a change request (send `reviewAnswers` keyed by point id, and any edited fields) puts it back in review. On a carrier rejection the edits are applied at the carrier and the identity is resubmitted straight away. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**update_branded_calling_identity_request** | [**UpdateBrandedCallingIdentityRequest**](UpdateBrandedCallingIdentityRequest.md) |  | [required] |

### Return type

[**models::BrandedCallingIdentity**](BrandedCallingIdentity.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

