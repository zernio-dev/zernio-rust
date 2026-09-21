# \IMessageApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_imessage_group_participant**](IMessageApi.md#add_imessage_group_participant) | **POST** /v1/imessage/groups/{conversationId}/participants | Add a participant to an iMessage group
[**cancel_imessage_sender**](IMessageApi.md#cancel_imessage_sender) | **DELETE** /v1/imessage/senders/{senderId} | Cancel an iMessage sender
[**create_imessage_group**](IMessageApi.md#create_imessage_group) | **POST** /v1/imessage/groups | Start an iMessage group chat
[**create_imessage_opt_in_link**](IMessageApi.md#create_imessage_opt_in_link) | **POST** /v1/imessage/senders/{senderId}/opt-in-links | Create a tracked iMessage opt-in link
[**get_imessage_group**](IMessageApi.md#get_imessage_group) | **GET** /v1/imessage/groups/{conversationId} | Get an iMessage group
[**get_imessage_sender**](IMessageApi.md#get_imessage_sender) | **GET** /v1/imessage/senders/{senderId} | Get iMessage sender status
[**list_imessage_audience**](IMessageApi.md#list_imessage_audience) | **GET** /v1/imessage/audience | List iMessage audience
[**list_imessage_available_numbers**](IMessageApi.md#list_imessage_available_numbers) | **GET** /v1/imessage/senders/available-numbers | List instantly available iMessage numbers
[**list_imessage_sender_orders**](IMessageApi.md#list_imessage_sender_orders) | **GET** /v1/imessage/senders/order | List iMessage sender orders
[**list_imessage_senders**](IMessageApi.md#list_imessage_senders) | **GET** /v1/imessage/senders | List iMessage senders
[**order_imessage_sender**](IMessageApi.md#order_imessage_sender) | **POST** /v1/imessage/senders/order | Order a new iMessage sender
[**register_imessage_sender**](IMessageApi.md#register_imessage_sender) | **POST** /v1/imessage/senders | Register an iMessage sender
[**remove_imessage_group_participant**](IMessageApi.md#remove_imessage_group_participant) | **DELETE** /v1/imessage/groups/{conversationId}/participants | Remove a participant from an iMessage group
[**reserve_imessage_available_number**](IMessageApi.md#reserve_imessage_available_number) | **POST** /v1/imessage/senders/available-numbers/{numberId}/reserve | Reserve an available iMessage number
[**set_imessage_subscription**](IMessageApi.md#set_imessage_subscription) | **POST** /v1/imessage/audience/subscription | Subscribe or opt out an iMessage contact
[**update_imessage_group**](IMessageApi.md#update_imessage_group) | **PATCH** /v1/imessage/groups/{conversationId} | Rename an iMessage group or change its photo
[**update_imessage_sender**](IMessageApi.md#update_imessage_sender) | **PATCH** /v1/imessage/senders/{senderId} | Update an iMessage sender



## add_imessage_group_participant

> models::AddImessageGroupParticipant200Response add_imessage_group_participant(conversation_id, add_imessage_group_participant_request)
Add a participant to an iMessage group

Applied asynchronously by the provider; the participant list on the next group webhook reflects it.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** |  | [required] |
**add_imessage_group_participant_request** | [**AddImessageGroupParticipantRequest**](AddImessageGroupParticipantRequest.md) |  | [required] |

### Return type

[**models::AddImessageGroupParticipant200Response**](addImessageGroupParticipant_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## cancel_imessage_sender

> models::OrderImessageSender202Response cancel_imessage_sender(sender_id)
Cancel an iMessage sender

Cancels the sender at the provider and deactivates its messaging account. Billing stops with the current month (no proration or refunds, matching phone numbers). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sender_id** | **String** |  | [required] |

### Return type

[**models::OrderImessageSender202Response**](orderImessageSender_202_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_imessage_group

> models::CreateImessageGroup202Response create_imessage_group(create_imessage_group_request)
Start an iMessage group chat

Creates a group chat from one of your senders and sends its first message. The provider processes it asynchronously: the response carries the request id, and the thread appears in the inbox (with its group conversation id) on the first webhook. Starting a group counts as messaging new contacts, so the sender needs the provider's init-conversations add-on and the same sending intervals apply; without it the request fails with 409 `recipient_must_message_first`. WhatsApp groups need a `name`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_imessage_group_request** | [**CreateImessageGroupRequest**](CreateImessageGroupRequest.md) |  | [required] |

### Return type

[**models::CreateImessageGroup202Response**](createImessageGroup_202_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_imessage_opt_in_link

> models::CreateImessageOptInLink200Response create_imessage_opt_in_link(sender_id, create_imessage_opt_in_link_request)
Create a tracked iMessage opt-in link

Generates a per-campaign link that opens Messages on this sender with `body` prefilled. iMessage is send-first: a sender can only message a contact who has written to it (a send to anyone else fails with `recipient_must_message_first`), and the contact's tap-and-send is what opens that door.  Each link carries a unique code in place of the `[opt-in-code]` placeholder; when the contact sends it, the resulting `message.received` webhook (and the stored inbox message's `metadata`) has `optIn: true` and your `parameters` under `optInParameters`, so you can attribute the conversation to the campaign or lead that produced it.  For an untracked link, use the sender's `optInLink` instead. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sender_id** | **String** |  | [required] |
**create_imessage_opt_in_link_request** | [**CreateImessageOptInLinkRequest**](CreateImessageOptInLinkRequest.md) |  | [required] |

### Return type

[**models::CreateImessageOptInLink200Response**](createImessageOptInLink_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_imessage_group

> models::GetImessageGroup200Response get_imessage_group(conversation_id, account_id)
Get an iMessage group

The group's name, participants and channel as the provider currently sees them. The conversation must be a group thread of the given account.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The inbox conversation id (or the provider group id) | [required] |
**account_id** | **String** |  | [required] |

### Return type

[**models::GetImessageGroup200Response**](getImessageGroup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_imessage_sender

> models::GetImessageSender200Response get_imessage_sender(sender_id)
Get iMessage sender status

Lifecycle status of an ordered or registered sender (poll while an order activates), plus the provider's live platform health for it.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sender_id** | **String** |  | [required] |

### Return type

[**models::GetImessageSender200Response**](getImessageSender_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_imessage_audience

> models::ListImessageAudience200Response list_imessage_audience(account_id, status, search, limit, skip)
List iMessage audience

Contacts who have messaged your iMessage senders (1:1 threads), with subscription state and, for threads opened through a tracked opt-in link, the parameters that brought them in. Newest activity first.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | Option<**String**> | Limit to one sender account |  |
**status** | Option<**String**> |  |  |
**search** | Option<**String**> | Matches the contact handle or name |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListImessageAudience200Response**](listImessageAudience_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_imessage_available_numbers

> models::ListImessageAvailableNumbers200Response list_imessage_available_numbers(region)
List instantly available iMessage numbers

Phone numbers the provider has already registered and can assign on the spot. Order one by passing its `id` as `availableNumberId` to POST /v1/imessage/senders/order: the sender activates immediately instead of after the usual provisioning wait. Reserve it first with POST /v1/imessage/senders/available-numbers/{numberId}/reserve while the buyer decides. The list is a snapshot; a number can be taken between listing and ordering. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**region** | Option<**String**> |  |  |

### Return type

[**models::ListImessageAvailableNumbers200Response**](listImessageAvailableNumbers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_imessage_sender_orders

> models::ListImessageSenderOrders200Response list_imessage_sender_orders(include_canceled)
List iMessage sender orders

Every sender lifecycle doc your team owns (ordered or registered), across statuses. Canceled senders are omitted unless `includeCanceled=true`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**include_canceled** | Option<**bool**> |  |  |[default to false]

### Return type

[**models::ListImessageSenderOrders200Response**](listImessageSenderOrders_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_imessage_senders

> models::ListImessageSenders200Response list_imessage_senders()
List iMessage senders

Lists the iMessage senders registered across your accessible profiles.

### Parameters

This endpoint does not need any parameter.

### Return type

[**models::ListImessageSenders200Response**](listImessageSenders_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## order_imessage_sender

> models::OrderImessageSender202Response order_imessage_sender(order_imessage_sender_request)
Order a new iMessage sender

Orders a NEW dedicated iMessage sender from the delivery provider (compare with POST /v1/imessage/senders, which registers a sender you already own). Activation is asynchronous (minutes to a few hours): the response is 202 with the lifecycle object; poll GET /v1/imessage/senders/{senderId} or subscribe to the account.connected webhook. Billing starts at activation (monthly per sender, no proration). Requires usage-based billing and a valid payment method. Pass purchaseIntentId to make retries idempotent — the provider-side order is never retried automatically. Ordered phone senders include SMS/RCS fallback with call forwarding and the ability to message contacts who have not written first (sending intervals still apply). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**order_imessage_sender_request** | [**OrderImessageSenderRequest**](OrderImessageSenderRequest.md) |  | [required] |

### Return type

[**models::OrderImessageSender202Response**](orderImessageSender_202_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## register_imessage_sender

> models::RegisterImessageSender200Response register_imessage_sender(register_imessage_sender_request)
Register an iMessage sender

Registers a provider-provisioned iMessage sender (a phone number or an email handle) that YOU already own on a profile, creating an `imessage` account that sends and receives through the inbox conversation endpoints. To have Zernio order a new sender for you, use POST /v1/imessage/senders/order instead. Registration attaches the monthly sender fee (billed while active) and requires a payment method (402 without one). One sender per profile: re-registering the SAME handle refreshes it; a different handle returns 409 until the existing sender is canceled. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**register_imessage_sender_request** | [**RegisterImessageSenderRequest**](RegisterImessageSenderRequest.md) |  | [required] |

### Return type

[**models::RegisterImessageSender200Response**](registerImessageSender_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_imessage_group_participant

> models::AddImessageGroupParticipant200Response remove_imessage_group_participant(conversation_id, account_id, contact)
Remove a participant from an iMessage group

Applied asynchronously by the provider.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** |  | [required] |
**account_id** | **String** |  | [required] |
**contact** | **String** | E.164 phone or iMessage email | [required] |

### Return type

[**models::AddImessageGroupParticipant200Response**](addImessageGroupParticipant_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reserve_imessage_available_number

> models::ReserveImessageAvailableNumber200Response reserve_imessage_available_number(number_id)
Reserve an available iMessage number

Holds the number for 3 minutes so nobody else can order it while the buyer decides. Place the order (POST /v1/imessage/senders/order with availableNumberId) before the hold expires. No request body.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**number_id** | **String** |  | [required] |

### Return type

[**models::ReserveImessageAvailableNumber200Response**](reserveImessageAvailableNumber_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_imessage_subscription

> models::SetImessageSubscription200Response set_imessage_subscription(set_imessage_subscription_request)
Subscribe or opt out an iMessage contact

Opted-out contacts are refused at send time (409 recipient_opted_out) until re-subscribed. Their inbound messages still arrive. Scoped to your account: it does not change the contact's state with other businesses.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**set_imessage_subscription_request** | [**SetImessageSubscriptionRequest**](SetImessageSubscriptionRequest.md) |  | [required] |

### Return type

[**models::SetImessageSubscription200Response**](setImessageSubscription_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_imessage_group

> models::UpdateImessageGroup200Response update_imessage_group(conversation_id, update_imessage_group_request)
Rename an iMessage group or change its photo

One change per call: either `name` or `photoUrl` (an empty `photoUrl` removes the photo). Applied asynchronously by the provider; a rename is mirrored on the inbox conversation right away.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** |  | [required] |
**update_imessage_group_request** | [**UpdateImessageGroupRequest**](UpdateImessageGroupRequest.md) |  | [required] |

### Return type

[**models::UpdateImessageGroup200Response**](updateImessageGroup_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_imessage_sender

> models::OrderImessageSender202Response update_imessage_sender(sender_id, update_imessage_sender_request)
Update an iMessage sender

Display name (inbox and API responses) and the contact card (vCard) recipients see when they save the sender. The contact card is what a contactCard send shares.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sender_id** | **String** |  | [required] |
**update_imessage_sender_request** | [**UpdateImessageSenderRequest**](UpdateImessageSenderRequest.md) |  | [required] |

### Return type

[**models::OrderImessageSender202Response**](orderImessageSender_202_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

