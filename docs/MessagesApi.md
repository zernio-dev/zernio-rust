# \MessagesApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_message_reaction**](MessagesApi.md#add_message_reaction) | **POST** /v1/inbox/conversations/{conversationId}/messages/{messageId}/reactions | Add reaction
[**delete_inbox_message**](MessagesApi.md#delete_inbox_message) | **DELETE** /v1/inbox/conversations/{conversationId}/messages/{messageId} | Delete message
[**edit_inbox_message**](MessagesApi.md#edit_inbox_message) | **PATCH** /v1/inbox/conversations/{conversationId}/messages/{messageId} | Edit message
[**get_inbox_conversation**](MessagesApi.md#get_inbox_conversation) | **GET** /v1/inbox/conversations/{conversationId} | Get conversation
[**get_inbox_conversation_messages**](MessagesApi.md#get_inbox_conversation_messages) | **GET** /v1/inbox/conversations/{conversationId}/messages | List messages
[**list_inbox_conversations**](MessagesApi.md#list_inbox_conversations) | **GET** /v1/inbox/conversations | List conversations
[**remove_message_reaction**](MessagesApi.md#remove_message_reaction) | **DELETE** /v1/inbox/conversations/{conversationId}/messages/{messageId}/reactions | Remove reaction
[**send_inbox_message**](MessagesApi.md#send_inbox_message) | **POST** /v1/inbox/conversations/{conversationId}/messages | Send message
[**send_typing_indicator**](MessagesApi.md#send_typing_indicator) | **POST** /v1/inbox/conversations/{conversationId}/typing | Send typing indicator
[**update_inbox_conversation**](MessagesApi.md#update_inbox_conversation) | **PUT** /v1/inbox/conversations/{conversationId} | Update conversation status
[**upload_media_direct**](MessagesApi.md#upload_media_direct) | **POST** /v1/media/upload-direct | Upload media file



## add_message_reaction

> models::UpdateYoutubeDefaultPlaylist200Response add_message_reaction(conversation_id, message_id, add_message_reaction_request)
Add reaction

Add an emoji reaction to a message. Platform support: - **Telegram**: Supports a subset of Unicode emoji reactions - **WhatsApp**: Supports any standard emoji (one reaction per message per sender) - **All others**: Returns 400 (not supported) 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID | [required] |
**message_id** | **String** | The platform message ID to react to | [required] |
**add_message_reaction_request** | [**AddMessageReactionRequest**](AddMessageReactionRequest.md) |  | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_inbox_message

> models::UpdateYoutubeDefaultPlaylist200Response delete_inbox_message(conversation_id, message_id, account_id)
Delete message

Delete a message from a conversation. Platform support varies: - **Telegram**: Full delete (bot's own messages anytime, others if admin) - **X/Twitter**: Full delete (own DM events only) - **Bluesky**: Delete for self only (recipient still sees it) - **Reddit**: Delete from sender's view only - **Facebook, Instagram, WhatsApp**: Not supported (returns 400) 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID | [required] |
**message_id** | **String** | The platform message ID to delete | [required] |
**account_id** | **String** | Social account ID | [required] |

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

Edit the text and/or reply markup of a previously sent Telegram message. Only supported for Telegram. Returns 400 for other platforms. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID | [required] |
**message_id** | **String** | The Telegram message ID to edit | [required] |
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
**conversation_id** | **String** | The conversation ID (id field from list conversations endpoint). This is the platform-specific conversation identifier, not an internal database ID. | [required] |
**account_id** | **String** | The social account ID | [required] |

### Return type

[**models::GetInboxConversation200Response**](getInboxConversation_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_inbox_conversation_messages

> models::GetInboxConversationMessages200Response get_inbox_conversation_messages(conversation_id, account_id)
List messages

Fetch messages for a specific conversation. Requires accountId query parameter.  **Twitter/X limitation:** X's encrypted \"X Chat\" messages are not accessible via the API. Conversations where the other participant uses encrypted X Chat may only show your outgoing messages. See the [list conversations endpoint](#/Messages/listInboxConversations) for more details. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID (id field from list conversations endpoint). This is the platform-specific conversation identifier, not an internal database ID. | [required] |
**account_id** | **String** | Social account ID | [required] |

### Return type

[**models::GetInboxConversationMessages200Response**](getInboxConversationMessages_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_inbox_conversations

> models::ListInboxConversations200Response list_inbox_conversations(profile_id, platform, status, sort_order, limit, cursor, account_id)
List conversations

Fetch conversations (DMs) from all connected messaging accounts in a single API call. Supports filtering by profile and platform. Results are aggregated and deduplicated. Supported platforms: Facebook, Instagram, Twitter/X, Bluesky, Reddit, Telegram.  **Twitter/X limitation:** X has replaced traditional DMs with encrypted \"X Chat\" for many accounts. Messages sent or received through encrypted X Chat are not accessible via X's API (the `/2/dm_events` endpoint only returns legacy unencrypted DMs). This means some Twitter/X conversations may show only outgoing messages or appear empty. This is an X platform limitation that affects all third-party applications. See [X's docs on encrypted messaging](https://help.x.com/en/using-x/about-chat) for more details. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> | Filter by profile ID |  |
**platform** | Option<**String**> | Filter by platform |  |
**status** | Option<**String**> | Filter by conversation status |  |
**sort_order** | Option<**String**> | Sort order by updated time |  |[default to desc]
**limit** | Option<**i32**> | Maximum number of conversations to return |  |[default to 50]
**cursor** | Option<**String**> | Pagination cursor for next page |  |
**account_id** | Option<**String**> | Filter by specific social account ID |  |

### Return type

[**models::ListInboxConversations200Response**](listInboxConversations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_message_reaction

> models::UpdateYoutubeDefaultPlaylist200Response remove_message_reaction(conversation_id, message_id, account_id)
Remove reaction

Remove a reaction from a message. Platform support: - **Telegram**: Send empty reaction array to clear - **WhatsApp**: Send empty emoji to remove - **All others**: Returns 400 (not supported) 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID | [required] |
**message_id** | **String** | The platform message ID | [required] |
**account_id** | **String** | Social account ID | [required] |

### Return type

[**models::UpdateYoutubeDefaultPlaylist200Response**](updateYoutubeDefaultPlaylist_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_inbox_message

> models::SendInboxMessage200Response send_inbox_message(conversation_id, send_inbox_message_request)
Send message

Send a message in a conversation. Supports text, attachments, quick replies, buttons, and message tags. Attachment and interactive message support varies by platform.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID (id field from list conversations endpoint). This is the platform-specific conversation identifier, not an internal database ID. | [required] |
**send_inbox_message_request** | [**SendInboxMessageRequest**](SendInboxMessageRequest.md) |  | [required] |

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

Show a typing indicator in a conversation. Platform support: - **Facebook Messenger**: Shows \"Page is typing...\" for 20 seconds - **Telegram**: Shows \"Bot is typing...\" for 5 seconds - **All others**: Returns 200 but no-op (platform doesn't support it)  Typing indicators are best-effort. The endpoint always returns 200 even if the platform call fails. 

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


## update_inbox_conversation

> models::UpdateInboxConversation200Response update_inbox_conversation(conversation_id, update_inbox_conversation_request)
Update conversation status

Archive or activate a conversation. Requires accountId in request body.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**conversation_id** | **String** | The conversation ID (id field from list conversations endpoint). This is the platform-specific conversation identifier, not an internal database ID. | [required] |
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

Upload a media file using API key authentication and get back a publicly accessible URL. The URL can be used as `attachmentUrl` when sending inbox messages.  Files are stored in temporary storage and auto-delete after 7 days. Maximum file size is 25MB.  Unlike `/v1/media/upload` (which uses upload tokens for end-user flows), this endpoint uses standard Bearer token authentication for programmatic use. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**file** | **std::path::PathBuf** | The file to upload (max 25MB) | [required] |
**content_type** | Option<**String**> | Override MIME type (e.g. \\\"image/jpeg\\\"). Auto-detected from file if not provided. |  |

### Return type

[**models::UploadMediaDirect200Response**](uploadMediaDirect_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

