# \SmsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**send_sms**](SmsApi.md#send_sms) | **POST** /v1/sms/messages | Send an SMS or MMS



## send_sms

> models::SendSms200Response send_sms(send_sms_request)
Send an SMS or MMS

Send a text (SMS) or media (MMS) message from one of your SMS-enabled numbers.  Provide `text`, `mediaUrls`, or both. Supply an `Idempotency-Key` header to make retries safe (a repeated key replays the original result instead of sending again). US numbers must have an approved carrier registration before they can deliver. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**send_sms_request** | [**SendSmsRequest**](SendSmsRequest.md) |  | [required] |

### Return type

[**models::SendSms200Response**](sendSms_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

