# \WebhookEventsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**on_account_connected**](WebhookEventsApi.md#on_account_connected) | **POST** /account.connected | Account connected event
[**on_account_disconnected**](WebhookEventsApi.md#on_account_disconnected) | **POST** /account.disconnected | Account disconnected event
[**on_comment_received**](WebhookEventsApi.md#on_comment_received) | **POST** /comment.received | Comment received event
[**on_message_deleted**](WebhookEventsApi.md#on_message_deleted) | **POST** /message.deleted | Message deleted event
[**on_message_delivered**](WebhookEventsApi.md#on_message_delivered) | **POST** /message.delivered | Message delivered event
[**on_message_edited**](WebhookEventsApi.md#on_message_edited) | **POST** /message.edited | Message edited event
[**on_message_failed**](WebhookEventsApi.md#on_message_failed) | **POST** /message.failed | Message delivery failed event
[**on_message_read**](WebhookEventsApi.md#on_message_read) | **POST** /message.read | Message read event
[**on_message_received**](WebhookEventsApi.md#on_message_received) | **POST** /message.received | Message received event
[**on_message_sent**](WebhookEventsApi.md#on_message_sent) | **POST** /message.sent | Message sent event
[**on_post_cancelled**](WebhookEventsApi.md#on_post_cancelled) | **POST** /post.cancelled | Post cancelled event
[**on_post_failed**](WebhookEventsApi.md#on_post_failed) | **POST** /post.failed | Post failed event
[**on_post_partial**](WebhookEventsApi.md#on_post_partial) | **POST** /post.partial | Post partial event
[**on_post_published**](WebhookEventsApi.md#on_post_published) | **POST** /post.published | Post published event
[**on_post_recycled**](WebhookEventsApi.md#on_post_recycled) | **POST** /post.recycled | Post recycled event
[**on_post_scheduled**](WebhookEventsApi.md#on_post_scheduled) | **POST** /post.scheduled | Post scheduled event
[**on_webhook_test**](WebhookEventsApi.md#on_webhook_test) | **POST** /webhook.test | Webhook test event



## on_account_connected

> on_account_connected(webhook_payload_account_connected)
Account connected event

Fired when a social account is successfully connected.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_account_connected** | [**WebhookPayloadAccountConnected**](WebhookPayloadAccountConnected.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_account_disconnected

> on_account_disconnected(webhook_payload_account_disconnected)
Account disconnected event

Fired when a connected social account becomes disconnected.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_account_disconnected** | [**WebhookPayloadAccountDisconnected**](WebhookPayloadAccountDisconnected.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_comment_received

> on_comment_received(webhook_payload_comment)
Comment received event

Fired when a new comment is received on a tracked post.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_comment** | [**WebhookPayloadComment**](WebhookPayloadComment.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_message_deleted

> on_message_deleted(webhook_payload_message_deleted)
Message deleted event

Fired when a sender deletes (unsends) a message. Supported on Instagram (incoming unsend) and WhatsApp (when the business deletes an outgoing message via the Cloud API). The payload retains the pre-delete text and attachments so API consumers can access the original content for moderation or compliance — the Zernio dashboard UI hides it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_message_deleted** | [**WebhookPayloadMessageDeleted**](WebhookPayloadMessageDeleted.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_message_delivered

> on_message_delivered(webhook_payload_message_delivery_status)
Message delivered event

Fired when an outgoing message is delivered to the recipient. Supported on WhatsApp and Facebook Messenger. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_message_delivery_status** | [**WebhookPayloadMessageDeliveryStatus**](WebhookPayloadMessageDeliveryStatus.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_message_edited

> on_message_edited(webhook_payload_message_edited)
Message edited event

Fired when a sender edits a previously-sent message. Supported on Instagram, Facebook Messenger, and Telegram. The payload includes the full editHistory so consumers can show prior versions. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_message_edited** | [**WebhookPayloadMessageEdited**](WebhookPayloadMessageEdited.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_message_failed

> on_message_failed(webhook_payload_message_delivery_status)
Message delivery failed event

Fired when an outgoing message fails to deliver. Currently only emitted for WhatsApp (other platforms don't expose per-message failure via webhook). The payload error object contains code, title, and message from the platform. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_message_delivery_status** | [**WebhookPayloadMessageDeliveryStatus**](WebhookPayloadMessageDeliveryStatus.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_message_read

> on_message_read(webhook_payload_message_delivery_status)
Message read event

Fired when an outgoing message is read by the recipient. Supported on WhatsApp, Facebook Messenger, and Instagram. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_message_delivery_status** | [**WebhookPayloadMessageDeliveryStatus**](WebhookPayloadMessageDeliveryStatus.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_message_received

> on_message_received(webhook_payload_message)
Message received event

Fired when a new inbox message is received.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_message** | [**WebhookPayloadMessage**](WebhookPayloadMessage.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_message_sent

> on_message_sent(webhook_payload_message_sent)
Message sent event

Fired when a message is sent via the API.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_message_sent** | [**WebhookPayloadMessageSent**](WebhookPayloadMessageSent.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_cancelled

> on_post_cancelled(webhook_payload_post)
Post cancelled event

Fired when a post publishing job is cancelled.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post** | [**WebhookPayloadPost**](WebhookPayloadPost.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_failed

> on_post_failed(webhook_payload_post)
Post failed event

Fired when a post fails to publish on all target platforms.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post** | [**WebhookPayloadPost**](WebhookPayloadPost.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_partial

> on_post_partial(webhook_payload_post)
Post partial event

Fired when a post publishes on some platforms and fails on others.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post** | [**WebhookPayloadPost**](WebhookPayloadPost.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_published

> on_post_published(webhook_payload_post)
Post published event

Fired when a post is successfully published.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post** | [**WebhookPayloadPost**](WebhookPayloadPost.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_recycled

> on_post_recycled(webhook_payload_post)
Post recycled event

Fired when a post is recycled (cloned and re-scheduled for publishing).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post** | [**WebhookPayloadPost**](WebhookPayloadPost.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_scheduled

> on_post_scheduled(webhook_payload_post)
Post scheduled event

Fired when a post is created and scheduled for publishing.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post** | [**WebhookPayloadPost**](WebhookPayloadPost.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_webhook_test

> on_webhook_test(webhook_payload_test)
Webhook test event

Fired when sending a test webhook to verify the endpoint configuration.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_test** | [**WebhookPayloadTest**](WebhookPayloadTest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

