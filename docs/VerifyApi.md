# \VerifyApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**check_verification**](VerifyApi.md#check_verification) | **POST** /v1/verify/verifications/{verificationId}/check | Check a verification code
[**create_verification**](VerifyApi.md#create_verification) | **POST** /v1/verify/verifications | Send a verification code
[**get_verification**](VerifyApi.md#get_verification) | **GET** /v1/verify/verifications/{verificationId} | Get a verification



## check_verification

> models::CheckVerification200Response check_verification(verification_id, check_verification_request)
Check a verification code

Verify the code the user typed. Wrong, expired, and exhausted codes answer 200 with `valid: false` and the settled `status` — only an unknown id is a 404. A correct code consumes the verification (single-use, `status: approved`) and fires the `verification.approved` webhook; the 5th wrong attempt settles it as `max_attempts_reached` and fires `verification.failed`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**verification_id** | **String** |  | [required] |
**check_verification_request** | [**CheckVerificationRequest**](CheckVerificationRequest.md) |  | [required] |

### Return type

[**models::CheckVerification200Response**](checkVerification_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_verification

> models::Verification create_verification(create_verification_request)
Send a verification code

Generate a one-time code, deliver it to the recipient, and store only its hash. Check the user-typed code with POST /v1/verify/verifications/{verificationId}/check.  Re-POSTing for the same (channel, to) while a verification is active RESENDS a fresh code on the existing verification (200 with `resend: true`) instead of creating a new one; resends are limited to one per 60 seconds (429 with `retryAfterSeconds` inside the cooldown). The stored brandName/codeLength/ttlMinutes win on a resend.  Codes deliver by SMS from a phone number on your account (`from` optional when you own exactly one SMS-enabled number) and the message uses a fixed template. Each accepted send bills one verification fee plus the standard message rate. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_verification_request** | [**CreateVerificationRequest**](CreateVerificationRequest.md) |  | [required] |

### Return type

[**models::Verification**](Verification.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_verification

> models::Verification get_verification(verification_id)
Get a verification

Current state of a verification. `status` is effective (a pending code past its expiry reads as `expired`). Verification records are deleted 24 hours after creation, after which this returns 404. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**verification_id** | **String** |  | [required] |

### Return type

[**models::Verification**](Verification.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

