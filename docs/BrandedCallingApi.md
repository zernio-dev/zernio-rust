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
[**resend_branded_calling_authorizer_code**](BrandedCallingApi.md#resend_branded_calling_authorizer_code) | **POST** /v1/branded-calling/identities/{id}/verify-email | Resend the authorizer's code
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

> models::BrandedCallingEnterprise create_branded_calling_enterprise(create_branded_calling_enterprise_request)
Register a business for Branded Calling

Stores the legal entity behind your caller identities. Nothing is filed with the carrier until the business's first identity passes review. Only businesses registered in the US or Canada qualify (a FEIN or Canadian equivalent is required); any other country returns `422`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_branded_calling_enterprise_request** | [**CreateBrandedCallingEnterpriseRequest**](CreateBrandedCallingEnterpriseRequest.md) |  | [required] |

### Return type

[**models::BrandedCallingEnterprise**](BrandedCallingEnterprise.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_branded_calling_identity

> models::BrandedCallingIdentity create_branded_calling_identity(create_branded_calling_identity_request)
Create a caller identity

A caller identity is what the callee sees: display name, logo and call reasons, backed by a registered business and three references the carrier vetting team phones. It starts in Zernio review (`requested`). Once approved, the carrier emails the authorizer a 6-digit code; confirm it with the verify-email endpoint and the identity goes into carrier vetting on its own. Track it with `GET` or the `branded_calling.identity.status_updated` webhook.  Billing: $100 per identity per month, the first month charged when the identity is filed with the carrier and not refunded if the carrier rejects it, then monthly while the identity exists. Branded calls add $0.10 each, counted on every outbound call from a verified branded number to a US destination (whether or not the callee's carrier displayed the branding); the surcharge shows as `brandedCallUSD` on the call's billing and in `GET /v1/voice/calls/estimate` when you pass `from`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_branded_calling_identity_request** | [**CreateBrandedCallingIdentityRequest**](CreateBrandedCallingIdentityRequest.md) |  | [required] |

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

