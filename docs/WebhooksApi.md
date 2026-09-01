# \WebhooksApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_webhook_settings**](WebhooksApi.md#create_webhook_settings) | **POST** /v1/webhooks/settings | Create webhook
[**delete_webhook_settings**](WebhooksApi.md#delete_webhook_settings) | **DELETE** /v1/webhooks/settings | Delete webhook
[**get_webhook_logs**](WebhooksApi.md#get_webhook_logs) | **GET** /v1/webhooks/logs | List webhook delivery logs
[**get_webhook_settings**](WebhooksApi.md#get_webhook_settings) | **GET** /v1/webhooks/settings | List webhooks
[**redeliver_webhook_event**](WebhooksApi.md#redeliver_webhook_event) | **POST** /v1/webhooks/logs/redeliver | Redeliver a webhook event
[**test_webhook**](WebhooksApi.md#test_webhook) | **POST** /v1/webhooks/test | Send test webhook
[**update_webhook_settings**](WebhooksApi.md#update_webhook_settings) | **PUT** /v1/webhooks/settings | Update webhook



## create_webhook_settings

> models::UpdateWebhookSettings200Response create_webhook_settings(create_webhook_settings_request)
Create webhook

Create a new webhook configuration. Maximum 50 webhooks per user.  `name`, `url` and `events` are required. `url` must be a valid URL and `events` must contain at least one event. Whitespace is trimmed from `url` before validation.  Webhooks are automatically disabled after 10 consecutive delivery failures.  A restricted (zrk_) API key can only subscribe to events whose resource group the key holds; an event outside the key's groups is rejected with 403, so a restricted key can never create a subscription broader than itself.  `disabledResourceGroups` restricts the subscription itself, independently of which key or session later reads it. Events in a disabled group are dropped before delivery to this endpoint, on live delivery and on every replay path (test fire, redelivery, dead-letter requeue), even if they are listed in `events`. Omit it to receive everything in `events`, which is how existing subscriptions behave. A restricted key's own disabled groups are always unioned in. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_webhook_settings_request** | [**CreateWebhookSettingsRequest**](CreateWebhookSettingsRequest.md) |  | [required] |

### Return type

[**models::UpdateWebhookSettings200Response**](updateWebhookSettings_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_webhook_settings

> models::UpdateYoutubeDefaultPlaylist200Response delete_webhook_settings(id)
Delete webhook

Permanently delete a webhook configuration.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**id** | **String** | Webhook ID to delete | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_webhook_logs

> models::GetWebhookLogs200Response get_webhook_logs(limit, skip, status, event, webhook_id, event_id)
List webhook delivery logs

Retrieve recorded webhook delivery attempts for the authenticated user, most recent first. Logs are retained for 30 days. Supports filtering by status, event type, webhook ID, and event ID, plus offset-based pagination.  For a restricted (zrk_) API key, rows for events outside the key's resource groups are omitted (`pagination.total` may over-count), and an `event` filter naming such an event is rejected with 403. Events blocked by a subscription's own `disabledResourceGroups` are dropped before delivery, so they produce no log rows for anyone; the exception is the five-minute tail after a denylist change, where an already-queued event can still be delivered and logged. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**limit** | Option<**i32**> | Maximum number of logs to return |  |[default to 50]
**skip** | Option<**i32**> | Number of logs to skip (offset-based pagination) |  |[default to 0]
**status** | Option<**String**> | Filter by delivery outcome |  |
**event** | Option<**String**> | Filter by event type (e.g. post.published) |  |
**webhook_id** | Option<**String**> | Filter by webhook configuration ID |  |
**event_id** | Option<**String**> | Filter by stable webhook event ID |  |

### Return type

[**models::GetWebhookLogs200Response**](getWebhookLogs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_webhook_settings

> models::GetWebhookSettings200Response get_webhook_settings()
List webhooks

Retrieve all configured webhooks for the authenticated user. Supports up to 50 webhooks per user.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::GetWebhookSettings200Response**](getWebhookSettings_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## redeliver_webhook_event

> models::UnpublishPost200Response redeliver_webhook_event(redeliver_webhook_event_request)
Redeliver a webhook event

Replay a past delivery: the original payload is re-sent, byte for byte, to the subscription's current URL. The original event ID is preserved so your endpoint can dedupe, and the replay is recorded as a fresh attempt, so it shows up in `GET /v1/webhooks/logs` next to the delivery it replays.  Both `webhookId` and `eventId` come from a row of `GET /v1/webhooks/logs`. Because the stored payload is replayed as-is, a redelivery reflects the event as it was emitted, not the current state of the resource.  Only deliveries inside the 30-day log retention window can be replayed; past that the payload is gone and the request fails with a 422. Replays run the same resource-group checks as live delivery, against both the key's groups and the subscription's `disabledResourceGroups`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**redeliver_webhook_event_request** | [**RedeliverWebhookEventRequest**](RedeliverWebhookEventRequest.md) |  | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## test_webhook

> models::UnpublishPost200Response test_webhook(test_webhook_request)
Send test webhook

Send a test webhook to verify your endpoint is configured correctly. The test payload includes event: \"webhook.test\" to distinguish it from real events.  `webhook.test` belongs to the `webhooks` resource group, so a key with that group disabled is rejected with 403, as is a test fire on a subscription that lists `webhooks` in its own `disabledResourceGroups` (a 403, not a reported delivery failure). Replays of real events (redelivery, dead-letter requeue) run the same checks as live delivery, against both the key's groups and the subscription's. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**test_webhook_request** | [**TestWebhookRequest**](TestWebhookRequest.md) |  | [required] |

### Return type

[**models::UnpublishPost200Response**](unpublishPost_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_webhook_settings

> models::UpdateWebhookSettings200Response update_webhook_settings(update_webhook_settings_request)
Update webhook

Update an existing webhook configuration. All fields except `_id` are optional; only provided fields will be updated.  When provided, `name` must be 1-50 characters, `url` must be a valid URL, and `events` must contain at least one event. Whitespace is trimmed from `url` before validation.  Webhooks are automatically disabled after 10 consecutive delivery failures.  A restricted (zrk_) API key can only set `events` to events whose resource group the key holds; an event outside the key's groups is rejected with 403. It also cannot widen an existing subscription past its own groups.  `disabledResourceGroups` replaces the subscription's own denylist, which applies to delivery regardless of which key or session created it. Send an empty array to clear it. A restricted key's own disabled groups are unioned into the stored value on every update, so repointing a legacy unrestricted subscription with a restricted key also narrows it.  Timing: the new denylist applies to every event emitted after the update. Events already queued for delivery when the update landed were filtered against the previous denylist and can still arrive at your endpoint for up to five minutes after they were enqueued, because the delivery worker trusts a five-minute enqueue-time snapshot before re-checking the subscription. Retries beyond that window, dead-letter replays, test fires, and redeliveries are all checked against the current denylist. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**update_webhook_settings_request** | [**UpdateWebhookSettingsRequest**](UpdateWebhookSettingsRequest.md) |  | [required] |

### Return type

[**models::UpdateWebhookSettings200Response**](updateWebhookSettings_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

