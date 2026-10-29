# \MessagesApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**accept_conversation_request**](MessagesApi.md#accept_conversation_request) | **POST** /v1/inbox/conversations/{conversationId}/accept | Accept a message request
[**add_conversation_label**](MessagesApi.md#add_conversation_label) | **POST** /v1/inbox/conversations/{conversationId}/labels | Add a label to a conversation
[**add_message_reaction**](MessagesApi.md#add_message_reaction) | **POST** /v1/inbox/conversations/{conversationId}/messages/{messageId}/reactions | Add reaction
[**create_inbox_conversation**](MessagesApi.md#create_inbox_conversation) | **POST** /v1/inbox/conversations | Create conversation
[**create_inbox_label**](MessagesApi.md#create_inbox_label) | **POST** /v1/inbox/labels | Create a conversation label
[**delete_inbox_conversation**](MessagesApi.md#delete_inbox_conversation) | **DELETE** /v1/inbox/conversations/{conversationId} | Delete conversation
[**delete_inbox_label**](MessagesApi.md#delete_inbox_label) | **DELETE** /v1/inbox/labels/{labelId} | Delete a conversation label
[**delete_inbox_message**](MessagesApi.md#delete_inbox_message) | **DELETE** /v1/inbox/conversations/{conversationId}/messages/{messageId} | Delete message
[**edit_inbox_message**](MessagesApi.md#edit_inbox_message) | **PATCH** /v1/inbox/conversations/{conversationId}/messages/{messageId} | Edit message
[**get_inbox_conversation**](MessagesApi.md#get_inbox_conversation) | **GET** /v1/inbox/conversations/{conversationId} | Get conversation
[**get_inbox_conversation_messages**](MessagesApi.md#get_inbox_conversation_messages) | **GET** /v1/inbox/conversations/{conversationId}/messages | List messages
[**get_message_attachment**](MessagesApi.md#get_message_attachment) | **GET** /v1/inbox/conversations/{conversationId}/messages/{messageId}/attachments/{index} | Resolve message attachment
[**list_conversation_labels**](MessagesApi.md#list_conversation_labels) | **GET** /v1/inbox/conversations/{conversationId}/labels | List the labels on a conversation
[**list_inbox_conversations**](MessagesApi.md#list_inbox_conversations) | **GET** /v1/inbox/conversations | List conversations
[**list_inbox_labels**](MessagesApi.md#list_inbox_labels) | **GET** /v1/inbox/labels | List the Page's conversation labels
[**mark_conversation_read**](MessagesApi.md#mark_conversation_read) | **POST** /v1/inbox/conversations/{conversationId}/read | Mark a conversation as read
[**remove_conversation_label**](MessagesApi.md#remove_conversation_label) | **DELETE** /v1/inbox/conversations/{conversationId}/labels/{labelId} | Remove a label from a conversation
[**remove_message_reaction**](MessagesApi.md#remove_message_reaction) | **DELETE** /v1/inbox/conversations/{conversationId}/messages/{messageId}/reactions | Remove reaction
[**search_inbox_conversations**](MessagesApi.md#search_inbox_conversations) | **GET** /v1/inbox/conversations/search | Search conversations
[**send_inbox_message**](MessagesApi.md#send_inbox_message) | **POST** /v1/inbox/conversations/{conversationId}/messages | Send message
[**send_typing_indicator**](MessagesApi.md#send_typing_indicator) | **POST** /v1/inbox/conversations/{conversationId}/typing | Send typing indicator
[**set_conversation_thread_control**](MessagesApi.md#set_conversation_thread_control) | **POST** /v1/inbox/conversations/{conversationId}/thread-control | Change who answers a conversation (handover)
[**update_inbox_conversation**](MessagesApi.md#update_inbox_conversation) | **PUT** /v1/inbox/conversations/{conversationId} | Update conversation status
[**upload_media_direct**](MessagesApi.md#upload_media_direct) | **POST** /v1/media/upload-direct | Upload media file



## accept_conversation_request

> models::AcceptConversationRequest200Response accept_conversation_request(conversation_id, accept_conversation_request_request)
Accept a message request

Accept a Facebook or Instagram Message Request by replying to it.  Facebook Page requests are listed with `GET /v1/inbox/conversations?folder=requests`; Instagram answers PLATFORM_LIMITATION there.  Meta has no separate accept call: the first reply is what moves the thread into the inbox. So this sends `message` through the same path, checks and webhooks as `POST /v1/inbox/conversations/{conversationId}/messages`, and answers the same way.  Supports the `Idempotency-Key` header. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The `id` of the request item from the requests folder. | [required] |
**accept_conversation_request_request** | [**AcceptConversationRequestRequest**](AcceptConversationRequestRequest.md) |  | [required] |

### Return type

[**models::AcceptConversationRequest200Response**](acceptConversationRequest_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## add_conversation_label

> models::UpdateYoutubeDefaultPlaylist200Response add_conversation_label(conversation_id, add_conversation_label_request)
Add a label to a conversation

Facebook Messenger only. Applies one of the Page's custom labels to the person in this conversation (Graph `POST /{label-id}/label?user={psid}`). The id must be one of the Page's custom labels, otherwise 404 `resource_not_found`. Other platforms answer 400 `platform_not_supported`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | Conversation ID (Zernio id or Meta platform conversation id) | [required] |
**add_conversation_label_request** | [**AddConversationLabelRequest**](AddConversationLabelRequest.md) |  | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## add_message_reaction

> models::AddMessageReaction200Response add_message_reaction(conversation_id, message_id, add_message_reaction_request)
Add reaction

Add an emoji reaction to a message.  ### Platform support  - Telegram: supports a subset of Unicode emoji reactions - WhatsApp: supports any standard emoji (one reaction per message per sender) - Instagram and Facebook Messenger: any standard emoji, subject to Meta's 24h messaging window - Slack: the emoji must have a Slack name (e.g. `:thumbsup:`); unnamed characters return 400 - iMessage: the six Apple tapbacks (❤️ 👍 👎 😂 ‼️ ❓) render natively; any other emoji is sent as a custom emoji tapback (iOS 18+ recipients) - All others: returns 400 (not supported) 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID | [required] |
**message_id** | **String** | The platform message ID (as returned by GET /messages) or the Zernio message ID (as returned by the reaction webhook) | [required] |
**add_message_reaction_request** | [**AddMessageReactionRequest**](AddMessageReactionRequest.md) |  | [required] |

### Return type

[**models::AddMessageReaction200Response**](addMessageReaction_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_inbox_conversation

> models::CreateInboxConversation201Response create_inbox_conversation(create_inbox_conversation_request)
Create conversation

Start a direct message conversation with a user. If a conversation with that recipient already exists, the message is added to the existing thread.  Supported platforms: X, Bluesky, Reddit, WhatsApp, SMS, Slack, iMessage, and email (Google and Microsoft accounts). Other platforms return PLATFORM_NOT_SUPPORTED.  ### Email (Google / Microsoft)  Pass the recipient address as participantId with `subject`, `message` and optionally `cc`. The mail is sent from the mailbox and mirrored into the inbox. The response names the inbox conversation it opened (the provider thread id, usable with the other inbox endpoints).  - 412 `account_scope_missing`: the account was connected without the `email` area - 409: the account is disconnected - 402 `payment_required`: Gmail accounts need a card on file  Sends count toward the mailbox's daily cap and never toward managed messages.  ### iMessage  Pass the recipient as participantId: a phone number in international format (+15551234567) or an iMessage email. Senders ordered through Zernio can message contacts who never wrote to them.  #### Opening message rules  The first message to such a contact must be plain text from an identifiable person or business opening a conversation.  A cold introduction, including a sales one, is fine (\"Hi Mark, this is John from Pratt Media. I help local roofers get more leads. Would you be open to a quick chat?\").  It may not contain links, email addresses, phone numbers, prices or attachments (the provider's own rule for opening messages). One that does returns 400 with code `invalid_content` and a message saying what was flagged, and nothing is sent.  #### New contact limits  Each sender may open at most one new conversation every 15 minutes. A new sender warms up, allowing this many new conversations per 24 hours:  - Days 1-2 after activation: 2 - Days 3-4: 5 - Days 5-7: 10 - Days 8-14: 20 - Days 15-21: 30 - After that: 50  Beyond that the request returns 429 with code `new_contact_limit` and a time to retry. The warm-up counts from when a sender ordered through Zernio went live. Senders registered from your own provider account are not warmed up by Zernio.  #### Follow-ups before the contact replies  Until the contact replies, the thread accepts the opening and at most two follow-ups, at least 24 hours apart.  - A follow-up sooner returns 429 `new_contact_limit` with the time to retry. - A fourth message returns 409 `recipient_must_message_first`.  The provider treats every message to a contact who has not replied as a new conversation.  Follow-ups therefore follow the same content rule and count toward the 15-minute spacing and the daily warm-up like an opening. Once the contact has written, the thread behaves like any other and is not limited.  #### Sender safety  Recipients can report a first message as junk, and reports can get a sender blocked permanently, so keep the reply rate high (above roughly 30%).  - A sender registered with your own provider account may lack the add-on for new contacts. Its sends to them return 409 `recipient_must_message_first`, and an opt-in link is the way in. - A contact who opted out returns 409 `recipient_opted_out`.  ### Slack  Pass a workspace member id as participantId (list them with GET /v1/accounts/{accountId}/slack-members). Zernio opens the DM channel with that member and sends the message. The thread then behaves like any other Slack conversation in the inbox. The member must belong to the connected workspace.  ### WhatsApp  This is the endpoint for sending an approved template message to a phone number. Put the recipient phone in participantId and provide:  - templateName - templateLanguage - templateParams: variable values for the text header, body and dynamic URL buttons, in that order  A template is required because WhatsApp does not permit freeform messages to open a conversation. A missing template returns TEMPLATE_REQUIRED.  #### Template lookup  Before sending, Zernio must resolve an exact APPROVED template definition matching both templateName and templateLanguage. If Meta rejects that lookup, or the exact approved definition is absent, Zernio sends no message and returns the canonical platform error instead.  Lookup errors use code `platform_api_error`, type `platform_error`, and platform `whatsapp`. Sanitized Meta code, message, and `error_data.details` are returned in `platformError`. `details` identifies `phase: template_lookup`, the query-free endpoint, upstream status, and only safe provider usage or retry headers.  #### Template headers, buttons and cards  - Templates with media headers (image, video, document) are handled automatically: Zernio fills the header at send time with the approved template's sample asset. - To send a DIFFERENT asset per message (e.g. a distinct invoice PDF for each recipient), pass headerMedia with a public link (or a Meta media id); it overrides the sample for that send. - A template whose approved header format is LOCATION has no header asset to reconstruct: Meta only accepts the location at send time. Pass headerLocation (latitude and longitude required) whenever such a template is sent. headerMedia and headerLocation cannot both be supplied. - A button that carries its own value at send time (a copy-code button holding a Pix payment code or a coupon, a flow token) is sent with templateButtonParams, addressed by the button's index. templateParams covers text variables and dynamic URL buttons only. - CAROUSEL templates take per-card overrides via templateCards, each addressed by the card's card_index. Card body variables restart at {{1}} per card and cannot be expressed in the flat templateParams order. - Template fields are accepted on the JSON body only, not on multipart requests.  #### Existing threads and the 24-hour window  For a number you already have a thread with, this sends the template into that thread. That makes it the way to re-engage a contact after the 24-hour customer-service window has closed. Once the recipient replies (opening the 24h window), send freeform messages with the send-message endpoint (POST /v1/inbox/conversations/{conversationId}/messages).  #### Meta Direct Send  WhatsApp Business Accounts eligible for Meta Direct Send can instead open a conversation with a business-initiated utility text message and no template. Pass category: 'utility' together with message (and no templateName). See the category field below.  ### X  #### DM eligibility  Before sending, the endpoint checks if the recipient accepts DMs from your account (via the receives_your_dm field). If not, a 422 error with code DM_NOT_ALLOWED is returned. Skip this check with skipDmCheck: true if you have already verified eligibility.  #### API tier requirement  DM write endpoints require X API Pro tier ($5,000/month) or Enterprise access. This applies to BYOK (Bring Your Own Key) users who provide their own X API credentials.  #### Rate limits (X only)  X's DM API enforces, shared across all DM endpoints:  - 200 requests per 15 minutes per connected X account - 1,000 per 24 hours per connected X account - 15,000 per 24 hours per X developer app  These limits do NOT apply to other platforms. WhatsApp sends are governed by Meta's per-number messaging tiers (unique business-initiated conversations per 24 hours) and per-number throughput instead. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_inbox_conversation_request** | [**CreateInboxConversationRequest**](CreateInboxConversationRequest.md) |  | [required] |

### Return type

[**models::CreateInboxConversation201Response**](createInboxConversation_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json, multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_inbox_label

> models::CreateInboxLabel201Response create_inbox_label(create_inbox_label_request)
Create a conversation label

Facebook Messenger only. Creates a custom label on the Page (Graph `POST /{page-id}/custom_labels`). Other platforms answer 400 `platform_not_supported`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_inbox_label_request** | [**CreateInboxLabelRequest**](CreateInboxLabelRequest.md) |  | [required] |

### Return type

[**models::CreateInboxLabel201Response**](createInboxLabel_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_inbox_conversation

> models::DeleteInboxConversation200Response delete_inbox_conversation(conversation_id, account_id)
Delete conversation

Permanently deletes Zernio's stored copy of one conversation and every message in it, in one transaction, and unlinks the contact channel that pointed at it.  ### What is kept  - Nothing is deleted on the platform (the thread stays in WhatsApp, Messenger or Instagram). - The contact record is kept: call DELETE /v1/contacts/{contactId} to erase the person's name and number as well.  Inbound media copies Zernio stored are removed on a best-effort basis.  ### Re-imports  A platform re-sync can import the thread again:  - WhatsApp coexistence numbers receive their messaging history from Meta repeatedly. - A Facebook or Instagram account whose DM history walk has not finished imports it on that walk. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | Opaque conversation identifier, accepted verbatim from the list endpoint or from the conversationId on inbox webhooks. Format not to be assumed. | [required] |
**account_id** | **String** | Account ID | [required] |

### Return type

[**models::DeleteInboxConversation200Response**](deleteInboxConversation_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_inbox_label

> models::UpdateYoutubeDefaultPlaylist200Response delete_inbox_label(label_id, account_id)
Delete a conversation label

Facebook Messenger only. Deletes a custom label from the Page (Graph `DELETE /{label-id}`), which also removes it from every conversation. The id must be one of the Page's custom labels, otherwise 404 `resource_not_found`. Other platforms answer 400 `platform_not_supported`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**label_id** | **String** | Meta label id | [required] |
**account_id** | **String** | Facebook social account ID | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_inbox_message

> models::UpdateYoutubeDefaultPlaylist200Response delete_inbox_message(conversation_id, message_id, account_id)
Delete message

Delete a message from a conversation. Platform support varies:  - Telegram: full delete (bot's own messages anytime, others if admin) - X: full delete (own DM events only) - Bluesky: delete for self only (recipient still sees it) - Reddit: delete from sender's view only - iMessage: unsend (the bubble disappears for the recipient) within 2 minutes of sending (Apple's limit; 409 `unsend_window_expired` after that). Own outbound messages only. - Facebook, Instagram, WhatsApp: not supported (returns 400) 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID | [required] |
**message_id** | **String** | The platform message ID to delete | [required] |
**account_id** | **String** | Account ID | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## edit_inbox_message

> models::EditInboxMessage200Response edit_inbox_message(conversation_id, message_id, edit_inbox_message_request)
Edit message

Edit a previously sent message. Platform support: - Telegram: text and/or reply markup, any time - 'iMessage: text only, within 15 minutes of sending (Apple''s limit; 409 `edit_window_expired` after that). Group messages included. The stored message keeps its edit history.' - All others: returns 400 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID | [required] |
**message_id** | **String** | The platform message ID to edit (iMessage also accepts the Zernio message id) | [required] |
**edit_inbox_message_request** | [**EditInboxMessageRequest**](EditInboxMessageRequest.md) |  | [required] |

### Return type

[**models::EditInboxMessage200Response**](editInboxMessage_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_inbox_conversation

> models::GetInboxConversation200Response get_inbox_conversation(conversation_id, account_id)
Get conversation

Retrieve details and metadata for a specific conversation. Requires accountId query parameter.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | Opaque conversation identifier, accepted verbatim from the list endpoint or from the conversationId on inbox webhooks. Format not to be assumed. | [required] |
**account_id** | **String** | The account ID | [required] |

### Return type

[**models::GetInboxConversation200Response**](getInboxConversation_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_inbox_conversation_messages

> models::GetInboxConversationMessages200Response get_inbox_conversation_messages(conversation_id, account_id, limit, cursor, sort_order)
List messages

Fetch messages for a specific conversation, with cursor-based pagination and ordering control.  ### Pagination  Pass `pagination.nextCursor` from a prior response back as the `cursor` query param to fetch the next page. The cursor is opaque; do not parse or construct it client-side.  ### Sort order  Defaults to `asc` (oldest first, chat style). For the \"show me the latest messages\" pattern, pass `?sortOrder=desc&limit=N`.  - X, Instagram, Telegram, WhatsApp and Reddit honor the requested order from the local message store. - Facebook and Bluesky upstream APIs only return newest-first and have no order parameter. Sort order is best-effort and only reverses items within a single page (pages still walk newest→oldest).  The response field `sortOrderApplied` tells you what was actually applied.  ### Platform limits  - **Reddit**: threads are paginated client-side because Reddit's API has no per-thread cursor. Very long threads may be upstream-truncated by Reddit's inbox/sent windows (~100 most-recent items each); this is a Reddit platform limitation. - **Instagram and Facebook**: conversations include history from before the account was connected, replayed from Meta. See below. - **X**: X's encrypted \"X Chat\" messages are not accessible via the API. Conversations where the other participant uses encrypted X Chat may only show your outgoing messages. See the list conversations endpoint for more details.  The Meta replay covers the 500 most recent messages per conversation: a longer thread keeps its newest 500 and older messages are not retrievable. Messages that arrived after the account was connected are unaffected. Replayed messages are stored as already read and emit no webhooks.  ### Read state  This endpoint is read-only and does NOT mark messages as read or send read receipts. To mark a conversation read (and send WhatsApp blue ticks on eligible accounts), call `POST /v1/inbox/conversations/{conversationId}/read`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | Opaque conversation identifier, accepted verbatim from the list endpoint or from the conversationId on inbox webhooks. Format not to be assumed. | [required] |
**account_id** | **String** | Account ID | [required] |
**limit** | Option<**i32**> | Number of messages to return per page. Default 100, max 100. |  |[default to 100]
**cursor** | Option<**String**> | Opaque pagination cursor. Pass `pagination.nextCursor` from a prior response verbatim: a cursor we cannot parse returns 400 rather than silently restarting from the first page. |  |
**sort_order** | Option<**String**> | Order of returned messages. Default `asc` (oldest first, chat style). X, Instagram, Telegram, WhatsApp and Reddit honor this order across cursor pages. For Facebook and Bluesky, only intra-page ordering is affected. Pages always walk newest→oldest. See `sortOrderApplied` in the response.  |  |[default to asc]

### Return type

[**models::GetInboxConversationMessages200Response**](getInboxConversationMessages_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_message_attachment

> models::GetMessageAttachment200Response get_message_attachment(conversation_id, message_id, index, account_id, format)
Resolve message attachment

Resolve one attachment on a message to a media url that works right now.  ### Why it exists  Instagram and Facebook sign DM media urls per request and expire them. So the `url` on a message is a snapshot: it works when you read the message and stops working later.  This endpoint checks the stored url and, when it has gone stale, re-mints the message's media from Meta and persists it before answering.  The message id never expires, so this URL is the one to store. It is returned ready-made on each attachment as `refreshUrl` when you read a message over REST.  ### Building the URL from a webhook  **Webhook payloads do not carry `refreshUrl`**, so a webhook-driven integration builds this URL itself. Every piece is in the event:  - `message.conversationId` - `message.platformMessageId` - the attachment's zero-based position - `account.accountId`  **`accountId` is a required query parameter**. Omitting it returns `400` `missing_required_field`, which is the same requirement `GET /v1/whatsapp/media/{mediaId}` has.  ### Response format  - By default it responds `302` to the live media url, so it can be used directly as an `<img src>` on a browser session. - API-key integrators should pass `?format=json` and read `url` off the body, since a browser cannot attach an Authorization header to an image request.  ### Other platforms  Only Instagram and Facebook media can be re-minted. On other platforms the stored url is returned as-is when it still resolves, and `404` otherwise. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID (Zernio id or platform conversation id) | [required] |
**message_id** | **String** | The message id as returned by the list-messages endpoint (the platform message id) | [required] |
**index** | **i32** | Zero-based position of the attachment in the message's attachments array | [required] |
**account_id** | **String** | Account ID. Required: without it the request returns 400 missing_required_field. | [required] |
**format** | Option<**String**> | `redirect` (default) answers 302 to the media; `json` returns the url in the body |  |[default to redirect]

### Return type

[**models::GetMessageAttachment200Response**](getMessageAttachment_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_conversation_labels

> models::ListInboxLabels200Response list_conversation_labels(conversation_id, account_id)
List the labels on a conversation

Facebook Messenger only. Lists the Page's custom labels applied to the person in this conversation (Graph `/{psid}/custom_labels`). Other platforms answer 400 `platform_not_supported`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | Conversation ID (Zernio id or Meta platform conversation id) | [required] |
**account_id** | **String** | Facebook social account ID | [required] |

### Return type

[**models::ListInboxLabels200Response**](listInboxLabels_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_inbox_conversations

> models::ListInboxConversations200Response list_inbox_conversations(profile_id, platform, status, folder, sort_order, limit, cursor, account_id)
List conversations

Fetch conversations (DMs) from all connected messaging accounts in a single API call. Supports filtering by profile and platform. Results are aggregated and deduplicated.  Supported platforms: Facebook, Instagram, X, Bluesky, Reddit, Telegram, WhatsApp, iMessage and SMS.  ### X limitation  X has replaced traditional DMs with encrypted \"X Chat\" for many accounts. Messages sent or received through encrypted X Chat are not accessible via X's API (the /2/dm_events endpoint only returns legacy unencrypted DMs).  This means some X conversations may show only outgoing messages or appear empty. This is an X platform limitation that affects all third-party applications. See X's docs on encrypted messaging for more details.  ### Instagram and Facebook pre-connect history  When one of these accounts is connected, Zernio replays the DM history the account already holds on Meta, so conversations that began before the account was connected appear here. Up to 500 conversations per account are replayed.  - The replay runs in the background and can finish after a listing you have already taken. - Replayed conversations keep their original lastMessageAt, so they sort into date order rather than appearing at the top. - If you mirror this endpoint into your own store, re-run the sweep rather than relying on a single pass at connect time. - Replayed history emits no webhooks and is stored as already read, so it never affects unread counts. - Threads that Meta refuses to serve are skipped. - An account whose Instagram \"connected tools\" message access is turned off is not replayed at all. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> | Filter by profile ID |  |
**platform** | Option<**String**> | Filter by platform |  |
**status** | Option<**String**> | Filter by conversation status |  |
**folder** | Option<**String**> | `requests` lists Facebook Page Message Requests (threads from people the account has not accepted) live from Meta, each item with `folder: requests`.  Meta has no accept call: replying moves a thread to the inbox, which is what POST /v1/inbox/conversations/{conversationId}/accept does.  - When Meta will not list the folder for the one account asked (`accountId`), the call answers 400 PLATFORM_LIMITATION. Across several accounts, the refusal is reported per account in meta.failedAccounts. - Instagram accounts (Instagram Login and Facebook Login) answer PLATFORM_LIMITATION, because Meta does not separate the folder on Instagram. Only Facebook Pages are served.  One page of up to `limit` threads. `pagination.hasMore` is true when threads past `limit` were cut (narrow with `accountId`). `pagination.nextCursor` is always null and a `cursor` answers 400.  |  |[default to inbox]
**sort_order** | Option<**String**> | Sort order by updated time |  |[default to desc]
**limit** | Option<**i32**> | Maximum number of conversations to return; values above 100 are served as 100. |  |[default to 50]
**cursor** | Option<**String**> | Pagination cursor for next page |  |
**account_id** | Option<**String**> | Filter by specific account ID |  |

### Return type

[**models::ListInboxConversations200Response**](listInboxConversations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_inbox_labels

> models::ListInboxLabels200Response list_inbox_labels(account_id)
List the Page's conversation labels

Facebook Messenger only. Lists the custom labels defined on the Page (Graph `/{page-id}/custom_labels`). Other platforms answer 400 `platform_not_supported`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Facebook social account ID | [required] |

### Return type

[**models::ListInboxLabels200Response**](listInboxLabels_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## mark_conversation_read

> models::MarkConversationRead200Response mark_conversation_read(conversation_id, send_typing_indicator_request)
Mark a conversation as read

Marks all unread incoming messages in the conversation as read.  For WhatsApp, this also sends read receipts (blue ticks) to the contact, EXCEPT on coexistence accounts (where the WhatsApp Business app on the customer's phone owns read state and we never override it).  For iMessage, this also marks the conversation read with the contact (1:1 conversations only). Best-effort.  For Instagram (Instagram Login and Facebook Login) and Facebook Messenger, this also sends a `mark_seen` read receipt to the contact, so they see the conversation as seen. Best-effort: a Meta failure never fails the request.  This is the explicit, human-driven counterpart to `GET .../messages`, which is side-effect-free and does NOT mark anything read. Call this when a user actually views the conversation. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID | [required] |
**send_typing_indicator_request** | [**SendTypingIndicatorRequest**](SendTypingIndicatorRequest.md) |  | [required] |

### Return type

[**models::MarkConversationRead200Response**](markConversationRead_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_conversation_label

> models::UpdateYoutubeDefaultPlaylist200Response remove_conversation_label(conversation_id, label_id, account_id)
Remove a label from a conversation

Facebook Messenger only. Removes one of the Page's custom labels from the person in this conversation (Graph `DELETE /{label-id}/label?user={psid}`). The label itself stays on the Page. The id must be one of the Page's custom labels, otherwise 404 `resource_not_found`. Other platforms answer 400 `platform_not_supported`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | Conversation ID (Zernio id or Meta platform conversation id) | [required] |
**label_id** | **String** | Meta label id | [required] |
**account_id** | **String** | Facebook social account ID | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_message_reaction

> models::RemoveMessageReaction200Response remove_message_reaction(conversation_id, message_id, account_id)
Remove reaction

Remove a reaction from a message.  ### Platform support  - Telegram: send empty reaction array to clear - WhatsApp: send empty emoji to remove - Instagram and Facebook Messenger: sends Meta's `unreact` action; the emoji does not need to be repeated - Slack: removes the reaction we previously sent on that message - iMessage: retracts your existing tapback or emoji reaction on the message (400 when you have none) - All others: returns 400 (not supported) 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID | [required] |
**message_id** | **String** | The platform message ID (as returned by GET /messages) or the Zernio message ID (as returned by the reaction webhook) | [required] |
**account_id** | **String** | Account ID | [required] |

### Return type

[**models::RemoveMessageReaction200Response**](removeMessageReaction_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## search_inbox_conversations

> models::SearchInboxConversations200Response search_inbox_conversations(query, direction, profile_id, platform, account_id, limit, cursor)
Search conversations

Search your conversations two ways at once, and get back the matching conversations, most-recent match first.  ### Message text  Matches words inside message bodies. Case-insensitive and accent-insensitive, exact tokens only (no substrings, no stemming). Each hit carries up to 3 most-recent matching messages.  With direction=outgoing you can collect examples of how you write to customers, for example to teach an AI agent your tone of voice.  ### Contact identity  Matches the participant's name, username, or phone number as a case-insensitive substring. These hits have matchCount 0 and an empty matches array.  A conversation that matches both ways is returned once, carrying its message matches.  ### Searchable platforms  Only platforms whose messages are stored by Zernio are searchable: WhatsApp, SMS, Telegram, Facebook, Instagram, X and Reddit.  Bluesky conversations are fetched live from the platform and cannot be searched; those accounts are listed in meta.accountsSkipped. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**query** | **String** | Text to search for, in message content and in the contact's name, username, or phone number | [required] |
**direction** | Option<**String**> | Only match messages sent to you (incoming) or by you (outgoing). Contact-identity matching is not applied when this is set. |  |
**profile_id** | Option<**String**> | Filter by profile ID |  |
**platform** | Option<**String**> | Filter by platform (searchable platforms only) |  |
**account_id** | Option<**String**> | Filter by specific account ID |  |
**limit** | Option<**i32**> | Maximum number of conversations to return |  |[default to 20]
**cursor** | Option<**String**> | Opaque pagination cursor. Pass back pagination.nextCursor verbatim; do not construct one. |  |

### Return type

[**models::SearchInboxConversations200Response**](searchInboxConversations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_inbox_message

> models::SendInboxMessage200Response send_inbox_message(conversation_id, send_inbox_message_request, idempotency_key)
Send message

Send a message in a conversation. Supports text, attachments, quick replies, buttons, templates, and message tags. Attachment and interactive message support varies by platform.  ### Email threads (Google / Microsoft accounts)  The text is sent as a reply to the latest mail of the thread, in either direction, with its recipients and a \"Re:\" subject. `cc` adds recipients. `message` is required.  - 400: attachments and `replyTo` are rejected here (use POST /v1/email/messages/{messageId}/reply for a reply with attachments) - 412 `account_scope_missing`: the account was connected without the `email` area - 409: the account is disconnected - 402: a Gmail account without a card on file  Mail sends count toward the mailbox's daily cap, never toward managed messages.  ### WhatsApp per-recipient rate limit  WhatsApp caps how many messages you may send to the same recipient in a short window. It rejects the excess with error code `131056` (\"Too many messages sent to this recipient\").  Pace sends to a single recipient at roughly 10 per minute; bursts above that return a `400` with code `131056`. Sends to other recipients are unaffected, so parallelise across recipients rather than flooding one.  ### iMessage pacing  Messages to contacts who have not written to the sender in the last 24 hours must be at least 2 minutes apart per sender.  A send inside that window returns `429` with code `new_contact_limit` and the time to retry. Replies to contacts who wrote within the last day are not paced.  A thread opened with `POST /v1/inbox/conversations` takes at most two follow-ups before the contact replies, at least 24 hours apart:  - `429 new_contact_limit`: a follow-up sent sooner - `409 recipient_must_message_first`: a fourth message  Each such follow-up counts as a new conversation:  - No links, emails, phone numbers, prices or attachments (`400 invalid_content`). - It uses the sender's 15-minute spacing and daily warm-up (`429 new_contact_limit`).  Text must be shorter than 10,000 characters.  ### WhatsApp template messages  To send an approved template into this conversation (required when the 24-hour customer-service window is closed), use the `template` field with a single element carrying the template reference: `{ \"elements\": [{ \"name\": ..., \"language\": ..., \"components\": [...] }] }`. See the `template` field below for the exact shape.  To send a template to a phone number you have no conversation with yet, use the create-conversation endpoint (POST /v1/inbox/conversations) instead.  #### Template lookup  Zernio resolves the exact APPROVED template name and language before any WhatsApp template send. A failed lookup or missing exact definition sends no message and returns code `platform_api_error`, type `platform_error`, and platform `whatsapp`.  Sanitized Meta code, message, and `error_data.details` are returned in `platformError`. `details` identifies `phase: template_lookup`, the query-free endpoint, upstream status, and only safe provider usage or retry headers.  ### WhatsApp interactive messages  Rich interactive messages (list, CTA URL, Flow, location request) are available via the `interactive` field. Tap events are delivered through the `message.received` webhook with WhatsApp-specific `metadata` fields (`interactiveType`, `interactiveId`, `flowResponseJson`, `flowResponseData`).  ### Idempotency  Send an `Idempotency-Key` header to make retries safe (e.g. after a client-side timeout where delivery is unknown). Works for JSON and multipart (file upload) requests alike. Keys are retained for 24 hours.  - Same key + same body: replays the original response (with `Idempotent-Replayed: true`) instead of sending the message a second time. - Same key + different body: returns 422. - A key still in flight: returns 409.  Only successful (2xx) responses are stored for replay. If the request throws or returns a non-2xx status, the key is released so the same key can be retried once the problem is fixed. The header therefore protects the \"request succeeded but the response was lost\" case.  For an ambiguous failure (a 5xx or a network timeout), reconcile before retrying. A failure after the platform already accepted the message also releases the key, so a blind retry could send it twice.  List the conversation's messages first. Treat an empty result as inconclusive rather than as proof nothing was sent, since a send that failed while being recorded leaves no trace on our side. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | Opaque conversation identifier, accepted verbatim from the list endpoint or from the conversationId on inbox webhooks. Format not to be assumed. | [required] |
**send_inbox_message_request** | [**SendInboxMessageRequest**](SendInboxMessageRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  |  |

### Return type

[**models::SendInboxMessage200Response**](sendInboxMessage_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json, multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_typing_indicator

> models::UpdateYoutubeDefaultPlaylist200Response send_typing_indicator(conversation_id, send_typing_indicator_request)
Send typing indicator

Show a typing indicator in a conversation.  ### Platform support  - Facebook Messenger: shows \"Page is typing...\" for 20 seconds. - Instagram: shows \"typing...\" to the recipient (works for both Instagram Login and Facebook Login accounts). The recipient must be signed in to Instagram to see it. - Telegram: shows \"Bot is typing...\" for 5 seconds. - WhatsApp: shows \"typing...\" for up to 25 seconds. Requires a recent inbound message in the conversation (Meta references the inbound message id) and also marks that message as read as a side-effect. - iMessage: shows a typing bubble for ~15 seconds (1:1 conversations only; requires a recent two-way exchange). - All others: returns 200 but no-op (platform doesn't support it).  ### Response  Typing indicators are best-effort. The endpoint always returns 200 even if the platform call fails.  `success` reports whether a typing indicator was actually sent to the platform (`false` on unsupported platforms or when the platform call failed). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID | [required] |
**send_typing_indicator_request** | [**SendTypingIndicatorRequest**](SendTypingIndicatorRequest.md) |  | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_conversation_thread_control

> models::SetConversationThreadControl200Response set_conversation_thread_control(conversation_id, set_conversation_thread_control_request)
Change who answers a conversation (handover)

Changes who answers a conversation, using Meta's handover protocol on WhatsApp, Facebook and Instagram.  **WhatsApp**, on numbers with Meta Business Agent enabled:  - `release`: hand the conversation back to the agent so it resumes answering. You must currently hold control (sending any message takes it implicitly). - `take`: take control before sending anything, so the agent stops replying while an operator reads the thread. Meta accepts this only from the business configured as the number's escalation partner; other apps take control by sending a message. - `pass`: transfer control to the number's configured escalation partner, or to the agent with `target: ai_agent`. Meta's Cloud API currently rejects it (\"Pass action is not supported\", verified 2026-09-08); use `release` to hand a thread back to the agent.  **Facebook and Instagram** (Messenger Platform handover between the apps on the Page, such as Page Inbox):  - `pass` with `targetAppId`: give the thread to another app (`pass_thread_control`). Page Inbox is 263902037430900. - `take`: take the thread back (`take_thread_control`). Meta allows it only to the Page's primary receiver, and only on accounts connected through a Facebook Page. On an Instagram Login connection it answers 400 `platform_not_supported`. - `request`: ask the current owner to pass the thread (`request_thread_control`); nothing changes until it does. Not available on Instagram Login connections (400 `platform_not_supported`). - `release`: give the thread back to the primary receiver (`release_thread_control`).  ### While another app owns the thread  While another app owns a Facebook or Instagram thread, inbound messages arrive with `metadata.standby: true` and a send answers 409 `not_thread_owner`.  The conversation's `threadControl` follows the result. A `conversation.control_changed` webhook fires when Meta later reports the change. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID | [required] |
**set_conversation_thread_control_request** | [**SetConversationThreadControlRequest**](SetConversationThreadControlRequest.md) |  | [required] |

### Return type

[**models::SetConversationThreadControl200Response**](setConversationThreadControl_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_inbox_conversation

> models::UpdateInboxConversation200Response update_inbox_conversation(conversation_id, update_inbox_conversation_request)
Update conversation status

Archive or activate a conversation. Requires accountId in request body.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | Opaque conversation identifier, accepted verbatim from the list endpoint or from the conversationId on inbox webhooks. Format not to be assumed. | [required] |
**update_inbox_conversation_request** | [**UpdateInboxConversationRequest**](UpdateInboxConversationRequest.md) |  | [required] |

### Return type

[**models::UpdateInboxConversation200Response**](updateInboxConversation_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upload_media_direct

> models::UploadMediaDirect200Response upload_media_direct(file, content_type)
Upload media file

Upload a media file using API key authentication and get back a publicly accessible URL. The URL can be used as attachmentUrl when sending inbox messages.  Files are stored in temporary storage and auto-delete after 7 days.  ### Size limit  The effective maximum is about 4.5 MB. The multipart body goes through the hosting platform's request body limit, which answers 413 before the endpoint's own 25 MB check is reached.  For larger files use POST /v1/media/presign and upload straight to storage.  ### Compared with /v1/media/upload  /v1/media/upload uses upload tokens for end-user flows. This endpoint takes your API key in the Authorization header, for programmatic use. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**file** | **std::path::PathBuf** | The file to upload (about 4.5 MB at most in practice; use POST /v1/media/presign for larger files) | [required] |
**content_type** | Option<**String**> | Override MIME type (e.g. \\\"image/jpeg\\\"). Auto-detected from file if not provided. |  |

### Return type

[**models::UploadMediaDirect200Response**](uploadMediaDirect_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

