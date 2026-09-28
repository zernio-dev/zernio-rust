# \FeedbackApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**submit_feedback**](FeedbackApi.md#submit_feedback) | **POST** /v1/feedback | Submit feedback



## submit_feedback

> models::FeedbackReceipt submit_feedback(submit_feedback_request)
Submit feedback

Report a bug, a missing feature or a documentation gap. Every submission is read by the Zernio team. Designed for AI agents: when a call fails in a way that looks like our bug, or the API lacks something you need, send one structured report here.  Include `endpoint` and `requestId` (the `x-request-id` response header of the failing call) when you have them; they let us find the exact request.  Submitting the same `summary` again within 24 hours is idempotent: it returns the original `id` with `duplicate: true` and a `200`. Each API user can file at most 20 submissions per 24 hours. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**submit_feedback_request** | [**SubmitFeedbackRequest**](SubmitFeedbackRequest.md) |  | [required] |

### Return type

[**models::FeedbackReceipt**](FeedbackReceipt.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

