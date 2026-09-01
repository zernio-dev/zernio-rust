# \WebhookEventsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**on_account_ads_initial_sync_completed**](WebhookEventsApi.md#on_account_ads_initial_sync_completed) | **POST** /account.ads.initial_sync_completed | Ads initial sync completed event
[**on_account_connected**](WebhookEventsApi.md#on_account_connected) | **POST** /account.connected | Account connected event
[**on_account_disconnected**](WebhookEventsApi.md#on_account_disconnected) | **POST** /account.disconnected | Account disconnected event
[**on_ad_status_changed**](WebhookEventsApi.md#on_ad_status_changed) | **POST** /ad.status_changed | Ad status changed event
[**on_call_ended**](WebhookEventsApi.md#on_call_ended) | **POST** /call.ended | Call ended event
[**on_call_failed**](WebhookEventsApi.md#on_call_failed) | **POST** /call.failed | Call failed event
[**on_call_permission_request**](WebhookEventsApi.md#on_call_permission_request) | **POST** /call.permission_request | Call permission request reply event
[**on_call_received**](WebhookEventsApi.md#on_call_received) | **POST** /call.received | Call received event
[**on_comment_received**](WebhookEventsApi.md#on_comment_received) | **POST** /comment.received | Comment received event
[**on_conversation_started**](WebhookEventsApi.md#on_conversation_started) | **POST** /conversation.started | Conversation started event
[**on_lead_received**](WebhookEventsApi.md#on_lead_received) | **POST** /lead.received | Lead received event
[**on_message_deleted**](WebhookEventsApi.md#on_message_deleted) | **POST** /message.deleted | Message deleted event
[**on_message_delivered**](WebhookEventsApi.md#on_message_delivered) | **POST** /message.delivered | Message delivered event
[**on_message_edited**](WebhookEventsApi.md#on_message_edited) | **POST** /message.edited | Message edited event
[**on_message_failed**](WebhookEventsApi.md#on_message_failed) | **POST** /message.failed | Message delivery failed event
[**on_message_read**](WebhookEventsApi.md#on_message_read) | **POST** /message.read | Message read event
[**on_message_received**](WebhookEventsApi.md#on_message_received) | **POST** /message.received | Message received event
[**on_message_sent**](WebhookEventsApi.md#on_message_sent) | **POST** /message.sent | Message sent event
[**on_phone_number_stock_available**](WebhookEventsApi.md#on_phone_number_stock_available) | **POST** /phone_number.stock_available | Phone-number stock available event
[**on_post_cancelled**](WebhookEventsApi.md#on_post_cancelled) | **POST** /post.cancelled | Post cancelled event
[**on_post_external_created**](WebhookEventsApi.md#on_post_external_created) | **POST** /post.external.created | External post created event
[**on_post_external_deleted**](WebhookEventsApi.md#on_post_external_deleted) | **POST** /post.external.deleted | External post deleted event
[**on_post_external_updated**](WebhookEventsApi.md#on_post_external_updated) | **POST** /post.external.updated | External post updated event
[**on_post_failed**](WebhookEventsApi.md#on_post_failed) | **POST** /post.failed | Post failed event
[**on_post_partial**](WebhookEventsApi.md#on_post_partial) | **POST** /post.partial | Post partial event
[**on_post_platform_deleted**](WebhookEventsApi.md#on_post_platform_deleted) | **POST** /post.platform.deleted | Post platform deleted event
[**on_post_platform_failed**](WebhookEventsApi.md#on_post_platform_failed) | **POST** /post.platform.failed | Post platform failed event
[**on_post_platform_published**](WebhookEventsApi.md#on_post_platform_published) | **POST** /post.platform.published | Post platform published event
[**on_post_published**](WebhookEventsApi.md#on_post_published) | **POST** /post.published | Post published event
[**on_post_recycled**](WebhookEventsApi.md#on_post_recycled) | **POST** /post.recycled | Post recycled event
[**on_post_scheduled**](WebhookEventsApi.md#on_post_scheduled) | **POST** /post.scheduled | Post scheduled event
[**on_post_tik_tok_url_resolved**](WebhookEventsApi.md#on_post_tik_tok_url_resolved) | **POST** /post.tiktok.url_resolved | TikTok post URL resolved event
[**on_reaction_received**](WebhookEventsApi.md#on_reaction_received) | **POST** /reaction.received | Reaction received event
[**on_referral_received**](WebhookEventsApi.md#on_referral_received) | **POST** /referral.received | Referral received event
[**on_review_new**](WebhookEventsApi.md#on_review_new) | **POST** /review.new | Review new event
[**on_review_updated**](WebhookEventsApi.md#on_review_updated) | **POST** /review.updated | Review updated event
[**on_verification_approved**](WebhookEventsApi.md#on_verification_approved) | **POST** /verification.approved | Verification approved event
[**on_verification_failed**](WebhookEventsApi.md#on_verification_failed) | **POST** /verification.failed | Verification failed event
[**on_webhook_test**](WebhookEventsApi.md#on_webhook_test) | **POST** /webhook.test | Webhook test event
[**on_whats_app_account_name_status_updated**](WebhookEventsApi.md#on_whats_app_account_name_status_updated) | **POST** /whatsapp.account.name_status_updated | WhatsApp display-name review outcome event
[**on_whats_app_automatic_event**](WebhookEventsApi.md#on_whats_app_automatic_event) | **POST** /whatsapp.automatic_event | WhatsApp automatic event detected
[**on_whats_app_number_action_required**](WebhookEventsApi.md#on_whats_app_number_action_required) | **POST** /whatsapp.number.action_required | WhatsApp number action required event
[**on_whats_app_number_activated**](WebhookEventsApi.md#on_whats_app_number_activated) | **POST** /whatsapp.number.activated | WhatsApp number activated event
[**on_whats_app_number_declined**](WebhookEventsApi.md#on_whats_app_number_declined) | **POST** /whatsapp.number.declined | WhatsApp number declined event
[**on_whats_app_number_kyc_submitted**](WebhookEventsApi.md#on_whats_app_number_kyc_submitted) | **POST** /whatsapp.number.kyc_submitted | WhatsApp number KYC submitted event
[**on_whats_app_number_reactivated**](WebhookEventsApi.md#on_whats_app_number_reactivated) | **POST** /whatsapp.number.reactivated | WhatsApp number reactivated event
[**on_whats_app_number_released**](WebhookEventsApi.md#on_whats_app_number_released) | **POST** /whatsapp.number.released | WhatsApp number released event
[**on_whats_app_number_suspended**](WebhookEventsApi.md#on_whats_app_number_suspended) | **POST** /whatsapp.number.suspended | WhatsApp number suspended event
[**on_whats_app_number_verification_required**](WebhookEventsApi.md#on_whats_app_number_verification_required) | **POST** /whatsapp.number.verification_required | WhatsApp number verification-required event
[**on_whats_app_template_category_updated**](WebhookEventsApi.md#on_whats_app_template_category_updated) | **POST** /whatsapp.template.category_updated | WhatsApp template category updated event
[**on_whats_app_template_status_updated**](WebhookEventsApi.md#on_whats_app_template_status_updated) | **POST** /whatsapp.template.status_updated | WhatsApp template status updated event



## on_account_ads_initial_sync_completed

> on_account_ads_initial_sync_completed(webhook_payload_account_ads_initial_sync_completed)
Ads initial sync completed event

Fired once per ads-enabled account when the initial sync (ad-account discovery + 90-day historical ad backfill) completes. The `sync` block reports whether the backfill succeeded and how many ads were synced. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_account_ads_initial_sync_completed** | [**WebhookPayloadAccountAdsInitialSyncCompleted**](WebhookPayloadAccountAdsInitialSyncCompleted.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


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


## on_ad_status_changed

> on_ad_status_changed(webhook_payload_ad_status_changed)
Ad status changed event

Fired when a campaign, ad set, or ad on a connected ad platform changes status. Currently emitted only for Meta (`metaads`).  Subscribed to two Meta `ad_account` webhook fields:   - `in_process_ad_objects` - the ad object finished processing and exited     the `IN_PROCESS` state. `status.raw` carries Meta's `status_name`     (e.g. `ACTIVE`, `PAUSED`, `ARCHIVED`, `DELETED`).   - `with_issues_ad_objects` - the ad object entered the `WITH_ISSUES`     state. `status.raw` is set to `WITH_ISSUES` and the `error` block is     populated from Meta's `error_code` / `error_summary` / `error_message`.  `adObject.level` mirrors Meta's `level` and is one of `CAMPAIGN`, `AD_SET`, or `AD`. Creative-level events are not forwarded.  Branch on `status.raw` to handle each transition; use `error.code` (when present) as the stable discriminator — `error.summary` and `error.message` are localized to the ad-account owner's Meta locale.  The `error` block is optional. It's present on most `WITH_ISSUES` events but can be absent (Meta does not always include diagnostics), and is never present on any other status. Always null-check `error` before reading `error.code`.  **Fan-out:** matching is keyed on `adObject.platformAdAccountId`. When multiple connected Zernio `metaads` accounts are linked to the same Meta ad account, each receives its own delivery. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_ad_status_changed** | [**WebhookPayloadAdStatusChanged**](WebhookPayloadAdStatusChanged.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_call_ended

> on_call_ended(webhook_payload_call_ended)
Call ended event

Fired on call hangup with the duration and a zero-markup billing breakdown (Meta cost, Telnyx cost, recording surcharge, total). Costs are pass-through; no margin is applied. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_call_ended** | [**WebhookPayloadCallEnded**](WebhookPayloadCallEnded.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_call_failed

> on_call_failed(webhook_payload_call_failed)
Call failed event

Fired when a call setup or in-progress call fails (Meta rejected the connect, Telnyx returned an error, etc.). Payload carries the upstream error code and message. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_call_failed** | [**WebhookPayloadCallFailed**](WebhookPayloadCallFailed.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_call_permission_request

> on_call_permission_request(webhook_payload_call_permission_request)
Call permission request reply event

Fired when a consumer replies to a `call_permission_request` interactive message (or its marketing-template variant). Carries the response (`accept` / `reject`), whether the grant is permanent, and the expiration timestamp when it is temporary. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_call_permission_request** | [**WebhookPayloadCallPermissionRequest**](WebhookPayloadCallPermissionRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_call_received

> on_call_received(webhook_payload_call_received)
Call received event

Fired when a WhatsApp Business Call connects. For inbound (UIC) calls the event fires at the moment our Telnyx trunk bridges the consumer leg to the customer&apos;s forward-to destination; for outbound (BIC) calls it fires immediately after Meta accepts the connect. Branch on `call.direction` to distinguish. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_call_received** | [**WebhookPayloadCallReceived**](WebhookPayloadCallReceived.md) |  | [required] |

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


## on_conversation_started

> on_conversation_started(webhook_payload_conversation_started)
Conversation started event

Fired once when a new conversation begins between one of your connected accounts and a contact, in either direction. Works across every DM platform (Instagram, Messenger/Facebook, Telegram, WhatsApp, Twitter, Reddit, Bluesky). Naturally deduped — a given conversation only fires this event the very first time it appears. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_conversation_started** | [**WebhookPayloadConversationStarted**](WebhookPayloadConversationStarted.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_lead_received

> on_lead_received(webhook_payload_lead)
Lead received event

Fired when a new lead is submitted against a Meta Lead Gen (Instant) Form and ingested via the Page `leadgen` webhook. `lead.fields` is the question-key to answer map; `lead.formId` / `lead.adId` give provenance. Requires the Ads add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_lead** | [**WebhookPayloadLead**](WebhookPayloadLead.md) |  | [required] |

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

Fired when a sender deletes (unsends) a message. Supported on Instagram (incoming unsend) and WhatsApp in both directions: an outgoing message the business deleted (via the Cloud API, or from the WhatsApp Business app on a Coexistence number) and an incoming message the customer deleted. Read `message.direction` to tell the two apart. The payload retains the pre-delete text and attachments so API consumers can access the original content for moderation or compliance; the Zernio dashboard UI hides it. 

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

Fired when a sender edits a previously-sent message. Supported on Instagram, Facebook Messenger, Telegram, and WhatsApp. The payload includes the full editHistory so consumers can show prior versions. 

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

Fired when a message is sent via the API, or from the WhatsApp Business app on Coexistence numbers. Sends that carry platform-specific context deliver it under `metadata`, so a quote-reply sent through the API arrives with `metadata.quotedMessageId` and mirroring CRMs can thread it without a lookup. Which surfaces actually carry that reference is documented on `WebhookPayloadMessageSent.metadata.quotedMessageId`; a quote-reply sent from the WhatsApp Business or Instagram app is not one of them. 

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


## on_phone_number_stock_available

> on_phone_number_stock_available(webhook_payload_phone_number_stock_available)
Phone-number stock available event

Fired by the stock sweep (every 6h) the first time a country you watch via POST /v1/phone-numbers/stock-watches has deliverable numbers again. The watch is consumed, so the event fires once per watch; the stock counts are a snapshot and numbers are sold first come, first served. Buy with POST /v1/phone-numbers/purchase. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_phone_number_stock_available** | [**WebhookPayloadPhoneNumberStockAvailable**](WebhookPayloadPhoneNumberStockAvailable.md) |  | [required] |

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


## on_post_external_created

> on_post_external_created(webhook_payload_external_post)
External post created event

Fired when Zernio's background sync detects a natively-authored post (created outside Zernio, e.g. a Google Business Profile localPost made in the Google UI) for the first time. Poll-driven (~hourly), not real-time. `post.source` is always \"external\". 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_external_post** | [**WebhookPayloadExternalPost**](WebhookPayloadExternalPost.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_external_deleted

> on_post_external_deleted(webhook_payload_external_post)
External post deleted event

Fired when a tracked native post is detected as removed from the platform. `post.deletedAt` carries the detection time. Coverage is bounded to the most recent posts the platform listing returns. Detection is a diff against the posts a prior sync already indexed, so an account for which no post has ever been indexed can never emit this event, no matter how the subscription is configured. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_external_post** | [**WebhookPayloadExternalPost**](WebhookPayloadExternalPost.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_external_updated

> on_post_external_updated(webhook_payload_external_post)
External post updated event

Fired when a tracked native post's text or media changed on the platform. Detected by comparing text/media structure and, where available, the platform's own edit timestamp; a media-URL-only refresh does not fire this. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_external_post** | [**WebhookPayloadExternalPost**](WebhookPayloadExternalPost.md) |  | [required] |

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


## on_post_platform_deleted

> on_post_platform_deleted(webhook_payload_post_platform)
Post platform deleted event

Fired when Zernio's background sync detects that a platform target published through Zernio was later deleted on the platform (e.g. the user deleted the Instagram post natively). Detection is poll-driven (~hourly), not real-time, and fires once per platform target. `platform.deletedAt` carries the detection time. Detection is listing-based: a false positive self-heals in Zernio's data when the post reappears, but the event is not retracted. Coverage is bounded to the posts the platform listing returns. Detection is a diff against the posts a prior sync already indexed, so an account for which no post has ever been indexed can never emit this event, no matter how the subscription is configured. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post_platform** | [**WebhookPayloadPostPlatform**](WebhookPayloadPostPlatform.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_platform_failed

> on_post_platform_failed(webhook_payload_post_platform)
Post platform failed event

Fired once per platform target inside a post as that platform fails permanently. Temporary/retryable failures do NOT fire this event — only permanent ones, so retry loops stay quiet. The envelope event (`post.failed` / `post.partial`) fires separately AFTER all platforms have terminated. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post_platform** | [**WebhookPayloadPostPlatform**](WebhookPayloadPostPlatform.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_platform_published

> on_post_platform_published(webhook_payload_post_platform)
Post platform published event

Fired once per platform target inside a post as that platform finishes publishing successfully. Does NOT wait for the post-level rollup — consumers building incremental UIs get notified immediately, even when other platforms on the same post are still processing. The envelope event (`post.published` / `post.partial`) fires separately AFTER all platforms have terminated. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post_platform** | [**WebhookPayloadPostPlatform**](WebhookPayloadPostPlatform.md) |  | [required] |

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

Fired when a post is recycled (cloned and re-scheduled for publishing). The new clone also fires a post.scheduled event.

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

Fired whenever a post enters the scheduled state: created with a schedule, added to a queue, a draft promoted to scheduled or queued, a failed or partial post retried, or a recycled clone created. Not fired when an already-scheduled post is edited or rescheduled.

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


## on_post_tik_tok_url_resolved

> on_post_tik_tok_url_resolved(webhook_payload_post_platform)
TikTok post URL resolved event

Fired when an already-published TikTok platform entry gets its public URL backfilled. TikTok exposes the numeric video id asynchronously (often minutes after PUBLISH_COMPLETE), so the terminal events can carry an empty `publishedUrl` for TikTok. This event delivers `platform.publishedUrl` and the resolved `platform.platformPostId` once available. At most once per platform target; never fires for drafts or private posts (no public URL exists). Payload shape is identical to `post.platform.published`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post_platform** | [**WebhookPayloadPostPlatform**](WebhookPayloadPostPlatform.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_reaction_received

> on_reaction_received(webhook_payload_reaction)
Reaction received event

Fired when a participant adds or removes an emoji reaction on a message. Supported on WhatsApp, Telegram, Slack, Instagram and Facebook Messenger. Distinct from message.received so a reaction (e.g. a thumbs-up) is not mistaken for an inbound message. The `reaction.action` field is `added` or `removed`. On WhatsApp and Meta removals the platform does not report which emoji was removed, so `reaction.emoji` may be an empty string. Instagram and Facebook accounts connected before reactions shipped only emit this event after their webhook subscription is refreshed; reconnect the account if reactions never arrive. Requires the Inbox add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_reaction** | [**WebhookPayloadReaction**](WebhookPayloadReaction.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_referral_received

> on_referral_received(webhook_payload_referral)
Referral received event

Fired when someone opens an EXISTING Instagram or Messenger thread through an attributable entry point - an ig.me / m.me link with a `ref` parameter, or (Messenger) a returning Click-to-Message ad click - which Meta delivers as a standalone referral with no message attached. A referral that rides an inbound message (first message of a thread, icebreaker taps, returning ad clicks on Instagram) arrives on `message.received` under `metadata.referral` instead; the two never fire for the same click. The first referral captured on a conversation is also persisted on it (see `metadata` on `GET /v1/inbox/conversations`). Requires the Inbox add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_referral** | [**WebhookPayloadReferral**](WebhookPayloadReferral.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_review_new

> on_review_new(webhook_payload_review_new)
Review new event

Fired when a new review is posted on a connected account. Currently supported for Google Business Profile (real-time via Pub/Sub). Requires the Inbox add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_review_new** | [**WebhookPayloadReviewNew**](WebhookPayloadReviewNew.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_review_updated

> on_review_updated(webhook_payload_review_updated)
Review updated event

Fired when a review changes: the reviewer edits their text or rating, or a reply is added (via the API or directly through the Google Business dashboard). Payload shape matches review.new. Requires the Inbox add-on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_review_updated** | [**WebhookPayloadReviewUpdated**](WebhookPayloadReviewUpdated.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_verification_approved

> on_verification_approved(on_verification_approved_request)
Verification approved event

Fired when a managed-OTP verification is approved (the user submitted the correct code to POST /v1/verify/verifications/{verificationId}/check). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_verification_approved_request** | [**OnVerificationApprovedRequest**](OnVerificationApprovedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_verification_failed

> on_verification_failed(on_verification_failed_request)
Verification failed event

Fired when a managed-OTP verification is exhausted (the maximum number of wrong code attempts was reached). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_verification_failed_request** | [**OnVerificationFailedRequest**](OnVerificationFailedRequest.md) |  | [required] |

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


## on_whats_app_account_name_status_updated

> on_whats_app_account_name_status_updated(webhook_payload_whats_app_account_name_status_updated)
WhatsApp display-name review outcome event

Fired when Meta finishes reviewing a WhatsApp Business display-name change. Forwarded from Meta's `phone_number_name_update` webhook field on the WhatsApp Business Account. Fires only on a review outcome (`name.status` APPROVED, DECLINED, or PENDING_REVIEW); a name applied without review reports `name_status: AVAILABLE_WITHOUT_REVIEW` on the phone node instead and produces no event here. `decision` REJECTED maps to DECLINED and DEFERRED maps to PENDING_REVIEW, matching the `name_status` vocabulary returned by `GET /v1/whatsapp/number-info`. Delivery is at-least-once; dedupe on `(account.accountId, name.status, name.requestedName)`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_whats_app_account_name_status_updated** | [**WebhookPayloadWhatsAppAccountNameStatusUpdated**](WebhookPayloadWhatsAppAccountNameStatusUpdated.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_automatic_event

> on_whats_app_automatic_event(on_whats_app_automatic_event_request)
WhatsApp automatic event detected

Fired when Meta's automatic event identification (opt-in during Embedded Signup; not available for EU/UK/JP businesses) detects a lead or purchase in a Click-to-WhatsApp conversation. Branch on `eventName` (`LeadSubmitted` | `Purchase`). Carries the `ctwa_clid` even on coexistence numbers where the inbound referral omits it (this webhook is the only surface that delivers it there); the clid is also written back onto the conversation, so POST /v1/whatsapp/conversions becomes usable for the thread. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_whats_app_automatic_event_request** | [**OnWhatsAppAutomaticEventRequest**](OnWhatsAppAutomaticEventRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_number_action_required

> on_whats_app_number_action_required(on_whats_app_number_action_required_request)
WhatsApp number action required event

Fired when the regulator asks for more information on an already-placed regulated number order. The number stays pending (nothing was rejected); the customer can provide the missing information from the dashboard, or via the remediation endpoint. `reason` carries the regulator's request verbatim when available. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_whats_app_number_action_required_request** | [**OnWhatsAppNumberActionRequiredRequest**](OnWhatsAppNumberActionRequiredRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_number_activated

> on_whats_app_number_activated(on_whats_app_number_activated_request)
WhatsApp number activated event

Fired when a purchased WhatsApp number becomes active and usable — both the synchronous (Tier 1/2) path and the asynchronous regulated (Tier 3/4) path land here. Lets integrators react without polling GET /v1/phone-numbers. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_whats_app_number_activated_request** | [**OnWhatsAppNumberActivatedRequest**](OnWhatsAppNumberActivatedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_number_declined

> on_whats_app_number_declined(on_whats_app_number_declined_request)
WhatsApp number declined event

Fired when a regulated (Tier 3/4) number order is declined or fails review. The number is never billed. `reason` carries the reviewer's rejection reason when available. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_whats_app_number_declined_request** | [**OnWhatsAppNumberDeclinedRequest**](OnWhatsAppNumberDeclinedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_number_kyc_submitted

> on_whats_app_number_kyc_submitted(on_whats_app_number_kyc_submitted_request)
WhatsApp number KYC submitted event

Fired when an end customer completes a hosted KYC share link (POST /v1/phone-numbers/kyc/share). The number enters review (pending_regulatory) under your account; `whatsapp.number.activated` or `whatsapp.number.declined` follows once the provider rules on it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_whats_app_number_kyc_submitted_request** | [**OnWhatsAppNumberKycSubmittedRequest**](OnWhatsAppNumberKycSubmittedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_number_reactivated

> on_whats_app_number_reactivated(on_whats_app_number_reactivated_request)
WhatsApp number reactivated event

Fired when a suspended number is reactivated (e.g. the payment recovered) and is usable again. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_whats_app_number_reactivated_request** | [**OnWhatsAppNumberReactivatedRequest**](OnWhatsAppNumberReactivatedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_number_released

> on_whats_app_number_released(on_whats_app_number_released_request)
WhatsApp number released event

Fired when a number is released and is no longer usable (by the user, a billing cleanup, or an admin). Terminal. `reason` carries the cause (e.g. `user_requested`, `cleanup_suspended`). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_whats_app_number_released_request** | [**OnWhatsAppNumberReleasedRequest**](OnWhatsAppNumberReleasedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_number_suspended

> on_whats_app_number_suspended(on_whats_app_number_suspended_request)
WhatsApp number suspended event

Fired when an active number is suspended (e.g. a failed payment). The number stops working until the issue is resolved, after which a `whatsapp.number.reactivated` event is sent. `reason` carries the cause (e.g. `payment_failed`, `subscription_ended`). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_whats_app_number_suspended_request** | [**OnWhatsAppNumberSuspendedRequest**](OnWhatsAppNumberSuspendedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_number_verification_required

> on_whats_app_number_verification_required(on_whats_app_number_verification_required_request)
WhatsApp number verification-required event

Fired when a regulated number has an out-of-band identity-verification step (e.g. Onfido). `verificationUrl` is the link to forward to the number's end user; the order completes once they pass. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_whats_app_number_verification_required_request** | [**OnWhatsAppNumberVerificationRequiredRequest**](OnWhatsAppNumberVerificationRequiredRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_template_category_updated

> on_whats_app_template_category_updated(webhook_payload_whats_app_template_category_updated)
WhatsApp template category updated event

Fired when Meta reclassifies a WhatsApp Business template's category after approval. Forwarded from Meta's `template_category_update` webhook field on the WhatsApp Business Account. Category drives Meta's per-conversation tariff and whether the template is subject to the recipient's marketing opt-out. `template.changeType` is `scheduled` (24h advance notice) or `applied`; `template.category` is always the category right now. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_whats_app_template_category_updated** | [**WebhookPayloadWhatsAppTemplateCategoryUpdated**](WebhookPayloadWhatsAppTemplateCategoryUpdated.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_template_status_updated

> on_whats_app_template_status_updated(webhook_payload_whats_app_template_status_updated)
WhatsApp template status updated event

Fired when Meta finishes (re)reviewing a WhatsApp Business template attached to a connected WABA. Forwarded from Meta's `message_template_status_update` webhook field on the WhatsApp Business Account. Consumers branch on `template.status` (APPROVED, REJECTED, PENDING, PAUSED, DISABLED, IN_APPEAL, PENDING_DELETION). Meta does not include the previous status or the template's category in this event. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_whats_app_template_status_updated** | [**WebhookPayloadWhatsAppTemplateStatusUpdated**](WebhookPayloadWhatsAppTemplateStatusUpdated.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

