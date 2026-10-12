# \SupportAssistantApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ask_support_question**](SupportAssistantApi.md#ask_support_question) | **POST** /v1/support/runs | Ask a support question (private beta)
[**get_support_answer**](SupportAssistantApi.md#get_support_answer) | **GET** /v1/support/runs/{runId} | Get a support answer (private beta)



## ask_support_question

> models::AskSupportQuestion202Response ask_support_question(ask_support_question_request, idempotency_key)
Ask a support question (private beta)

Private beta: returns 403 `feature_not_available` unless enabled for your account. Asks Ana, the Zernio support agent, a question about your workspace. Each question starts a run that answers asynchronously: this returns 202 with a `runId`, and the answer arrives through the `support.run.completed` and `support.run.failed` webhooks. `GET /v1/support/runs/{runId}` is the fallback. Pass `threadId` to continue an earlier conversation, and `context` to point Ana at a post, account or profile. Billed when the run finishes at the model cost plus 20%, never above `maxCostUsd`; failed runs are free. When Ana finds a problem on Zernio's side she opens a support ticket with the team (see `supportTicket` on the run) and the run ends as `needs_human`. Requires an unrestricted API key, usage-based billing and a card on file. Limits per account: 3 active runs and $100 of runs per UTC month. Send an Idempotency-Key header to make retries safe.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ask_support_question_request** | [**AskSupportQuestionRequest**](AskSupportQuestionRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. |  |

### Return type

[**models::AskSupportQuestion202Response**](askSupportQuestion_202_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_support_answer

> models::SupportRun get_support_answer(run_id)
Get a support answer (private beta)

Private beta: returns 403 `feature_not_available` unless enabled for your account. Returns a run started by your team, with Ana's answer once it is ready. Prefer the `support.run.completed` and `support.run.failed` webhooks; use this as the fallback, waiting `pollAfterSeconds` between polls. `costUsd` is the amount billed: the model cost plus 20%, never above `maxCostUsd`, and 0 for a failed run.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**run_id** | **String** |  | [required] |

### Return type

[**models::SupportRun**](SupportRun.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

