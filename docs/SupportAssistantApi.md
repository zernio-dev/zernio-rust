# \SupportAssistantApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ask_support_question**](SupportAssistantApi.md#ask_support_question) | **POST** /v1/support/runs | Ask a support question
[**get_support_answer**](SupportAssistantApi.md#get_support_answer) | **GET** /v1/support/runs/{runId} | Get a support answer
[**list_support_answers**](SupportAssistantApi.md#list_support_answers) | **GET** /v1/support/runs | List a thread's support answers



## ask_support_question

> models::AskSupportQuestion202Response ask_support_question(ask_support_question_request, idempotency_key)
Ask a support question

Asks the Zernio Support Assistant a question about your workspace. Each question starts a run that answers asynchronously: this returns 202 with a `runId`, and the answer arrives through the `support.run.completed` and `support.run.failed` webhooks. `GET /v1/support/runs/{runId}` is the fallback. Pass `threadId` to continue an earlier conversation, and `context` to point the assistant at a post, account, profile or a failed request (its `X-Request-Id`). When the assistant finds a problem on Zernio's side it opens a support ticket with the team (see `supportTicket` on the run) and the run ends as `needs_human`.  **Pricing.** You pay per question, once it finishes. The exact amount charged is the run's `costUsd`.  | Question | You pay | | --- | --- | | Typical question | $0.10 to $0.50 | | Most one question can cost | Its `maxCostUsd`: $0.50 to $3, $3 by default | | Handed to the Zernio team (`needs_human`) | Charged like an answered question | | Failed or expired | $0 | | All questions in a UTC month | At most $100 per account |  Near its `maxCostUsd` a run stops investigating and answers with what it found so far, so it never charges more than the cap; with nothing to answer yet it fails and costs nothing. Charges appear as \"Support API\" on your invoice.  Requires an unrestricted API key, usage-based billing and a card on file. Limits per account: 3 active runs and $100 of runs per UTC month. Send an Idempotency-Key header to make retries safe. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**ask_support_question_request** | [**AskSupportQuestionRequest**](AskSupportQuestionRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe. Same key + same body replays the original response; same key + different body → 422; key still processing → 409. A request cut off mid-handler (for example by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours. |  |

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
Get a support answer

Returns a run started by your team, with the answer once it is ready. Prefer the `support.run.completed` and `support.run.failed` webhooks; use this as the fallback, waiting `pollAfterSeconds` between polls. `costUsd` is the amount billed for the question, never above `maxCostUsd`, and 0 for a failed run (pricing on Ask a support question).

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


## list_support_answers

> models::ListSupportAnswers200Response list_support_answers(thread_id, limit, cursor)
List a thread's support answers

Lists the runs of one thread that your team started, with each question and its answer, oldest first. Replies from the Zernio team after a support ticket arrive by email and are not included. Runs are kept for 90 days. Page through a long thread with `limit` and `cursor`: pass `nextCursor` as `cursor` until it is null.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**thread_id** | **String** | The thread to list, as returned by `POST /v1/support/runs`. | [required] |
**limit** | Option<**i32**> | Runs per page. |  |[default to 20]
**cursor** | Option<**String**> | Pass `nextCursor` from the previous page. |  |

### Return type

[**models::ListSupportAnswers200Response**](listSupportAnswers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

