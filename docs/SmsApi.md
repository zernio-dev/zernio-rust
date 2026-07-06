# \SmsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**appeal_sms_registration**](SmsApi.md#appeal_sms_registration) | **POST** /v1/sms/registrations/{id}/appeal | Appeal a rejected campaign
[**disable_sms_on_number**](SmsApi.md#disable_sms_on_number) | **DELETE** /v1/phone-numbers/{id}/sms | Disable SMS on a number
[**enable_sms_on_number**](SmsApi.md#enable_sms_on_number) | **POST** /v1/phone-numbers/{id}/sms | Enable SMS on a number
[**get_sms_registration**](SmsApi.md#get_sms_registration) | **GET** /v1/sms/registrations/{id} | Get a carrier registration
[**list_sms_opt_outs**](SmsApi.md#list_sms_opt_outs) | **GET** /v1/sms/opt-outs | List SMS opt-outs
[**list_sms_registrations**](SmsApi.md#list_sms_registrations) | **GET** /v1/sms/registrations | List carrier registrations
[**lookup_sms_number**](SmsApi.md#lookup_sms_number) | **GET** /v1/sms/lookup | Look up carrier + line type
[**reuse_sms_registration_for_number**](SmsApi.md#reuse_sms_registration_for_number) | **POST** /v1/phone-numbers/{id}/sms/reuse-registration | Add a number to an existing registration
[**send_sms**](SmsApi.md#send_sms) | **POST** /v1/sms/messages | Send an SMS/MMS
[**share_sms_registration**](SmsApi.md#share_sms_registration) | **POST** /v1/sms/registrations/share | Create a registration share link
[**start_sms_registration**](SmsApi.md#start_sms_registration) | **POST** /v1/sms/registrations | Start a carrier registration
[**verify_sms_registration_otp**](SmsApi.md#verify_sms_registration_otp) | **POST** /v1/sms/registrations/{id}/verify-otp | Submit the sole-prop OTP



## appeal_sms_registration

> models::AppealSmsRegistration200Response appeal_sms_registration(id, appeal_sms_registration_request)
Appeal a rejected campaign

Appeals a rejected 10DLC campaign with the carrier registry. Only a registration that reached campaign creation can be appealed; a brand-level rejection should be fixed and re-verified instead. On success the registration returns to `pending`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**appeal_sms_registration_request** | [**AppealSmsRegistrationRequest**](AppealSmsRegistrationRequest.md) |  | [required] |

### Return type

[**models::AppealSmsRegistration200Response**](appealSmsRegistration_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## disable_sms_on_number

> models::DisableSmsOnNumber200Response disable_sms_on_number(id)
Disable SMS on a number

Turns off SMS for the number (deactivates its SMS account). The carrier registration is untouched, so re-enabling later just reactivates it, with no re-registration. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::DisableSmsOnNumber200Response**](disableSmsOnNumber_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## enable_sms_on_number

> models::EnableSmsOnNumber200Response enable_sms_on_number(id)
Enable SMS on a number

Turns on SMS for one of your numbers. The number's real carrier capability is checked first: some number types can't do SMS at all (`smsCapable: false`), and a number still provisioning at the carrier returns `notReady: true` (try again once provisioning finishes).  US numbers additionally need a carrier registration before messages deliver; the response tells you which path applies: - `alreadyRegistered: true`: a prior registration still covers this   number; SMS was simply reactivated. - `reusable` set: you have an approved registration this number can   join in one click via   `POST /v1/phone-numbers/{id}/sms/reuse-registration`   (no new brand/campaign, no extra carrier fee). - `needsRegistration: true` and no `reusable`: start one via   `POST /v1/sms/registrations`.  Idempotent: re-running re-attempts any carrier-side setup that failed. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Phone number record ID (from GET /v1/phone-numbers). | [required] |

### Return type

[**models::EnableSmsOnNumber200Response**](enableSmsOnNumber_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_sms_registration

> models::GetSmsRegistration200Response get_sms_registration(id)
Get a carrier registration

Poll this for approval progress after starting a registration.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::GetSmsRegistration200Response**](getSmsRegistration_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_sms_opt_outs

> models::ListSmsOptOuts200Response list_sms_opt_outs(format, limit)
List SMS opt-outs

The recipients who opted out of SMS (replied STOP) across your numbers, most recent first. Compliance surface: you must be able to see and export your opt-out list. Read-only: a recipient is re-subscribed only by replying START. Pass `format=csv` to download a CSV instead of JSON. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**format** | Option<**String**> |  |  |[default to json]
**limit** | Option<**i32**> |  |  |[default to 500]

### Return type

[**models::ListSmsOptOuts200Response**](listSmsOptOuts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json, text/csv

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_sms_registrations

> models::ListSmsRegistrations200Response list_sms_registrations()
List carrier registrations

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListSmsRegistrations200Response**](listSmsRegistrations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## lookup_sms_number

> models::LookupSmsNumber200Response lookup_sms_number(number)
Look up carrier + line type

Carrier name and line type (mobile / landline / voip / toll-free) for a number, plus `smsReachable` (landlines can't receive SMS). Use it to validate recipients before sending. Each lookup is billed by the carrier-data provider, so call it explicitly (e.g. pre-validating an opt-in list), not on every send. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**number** | **String** | Number to look up (E.164; formatting is normalized). | [required] |

### Return type

[**models::LookupSmsNumber200Response**](lookupSmsNumber_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reuse_sms_registration_for_number

> models::ReuseSmsRegistrationForNumber200Response reuse_sms_registration_for_number(id)
Add a number to an existing registration

Attaches this number to your existing approved 10DLC campaign instead of running a fresh registration: the number inherits the campaign's approval (no new brand or campaign, no extra carrier fee). Enable SMS on the number first (`POST /v1/phone-numbers/{id}/sms`; its response tells you whether a reusable registration exists). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |

### Return type

[**models::ReuseSmsRegistrationForNumber200Response**](reuseSmsRegistrationForNumber_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_sms

> models::SendSms200Response send_sms(send_sms_request, idempotency_key)
Send an SMS/MMS

Sends an SMS (or MMS when `mediaUrls` is set) from one of your SMS-enabled numbers. At least one of `text` / `mediaUrls` is required. Both numbers are normalized to E.164, so `from` matches regardless of formatting and replies thread into the same inbox conversation.  US numbers must have an approved carrier registration (`/v1/sms/registrations`) before messages deliver.  **Idempotency:** send an `Idempotency-Key` header to make retries safe: same key + same body replays the original response instead of sending a second message; same key + different body returns 422; a key still in flight returns 409. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**send_sms_request** | [**SendSmsRequest**](SendSmsRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes send retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. |  |

### Return type

[**models::SendSms200Response**](sendSms_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## share_sms_registration

> models::ShareSmsRegistration200Response share_sms_registration(share_sms_registration_request)
Create a registration share link

Creates a single-use, expiring link (valid 7 days) that lets someone else (whoever has the legal business details) fill in the carrier registration form for one of your numbers, without a Zernio login. The registration is created under your account once the form is submitted. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**share_sms_registration_request** | [**ShareSmsRegistrationRequest**](ShareSmsRegistrationRequest.md) |  | [required] |

### Return type

[**models::ShareSmsRegistration200Response**](shareSmsRegistration_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## start_sms_registration

> models::StartSmsRegistration200Response start_sms_registration(start_sms_registration_request)
Start a carrier registration

Starts the US carrier registration that a number needs before SMS delivers: 10DLC (standard company or sole-proprietor) or toll-free verification. 10DLC needs `brand` + `campaign`; toll-free needs `tollFree`. Approval is asynchronous; poll `GET /v1/sms/registrations/{id}` (sole-prop registrations first need the OTP step: a code is texted to the brand's mobile number, submit it via `/verify-otp`).  Already have an approved registration? Add another number to it with `POST /v1/phone-numbers/{id}/sms/reuse-registration` instead of registering (and paying the carrier brand fee) again.  Rather have your client fill in the legal business details? Create a share link with `POST /v1/sms/registrations/share`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**start_sms_registration_request** | [**StartSmsRegistrationRequest**](StartSmsRegistrationRequest.md) |  | [required] |

### Return type

[**models::StartSmsRegistration200Response**](startSmsRegistration_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## verify_sms_registration_otp

> models::VerifySmsRegistrationOtp200Response verify_sms_registration_otp(id, verify_sms_registration_otp_request)
Submit the sole-prop OTP

Completes sole-proprietor 10DLC brand verification by submitting the one-time PIN texted to the brand's mobile number. On success the registration continues to campaign creation automatically. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** |  | [required] |
**verify_sms_registration_otp_request** | [**VerifySmsRegistrationOtpRequest**](VerifySmsRegistrationOtpRequest.md) |  | [required] |

### Return type

[**models::VerifySmsRegistrationOtp200Response**](verifySmsRegistrationOtp_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

