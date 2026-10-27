# \EmailApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**download_email_attachment**](EmailApi.md#download_email_attachment) | **GET** /v1/email/attachments/{attachmentId} | Download an attachment
[**get_email_message**](EmailApi.md#get_email_message) | **GET** /v1/email/messages/{messageId} | Get an email message
[**get_email_thread**](EmailApi.md#get_email_thread) | **GET** /v1/email/threads/{threadId} | Get an email thread with its messages
[**list_email_folders**](EmailApi.md#list_email_folders) | **GET** /v1/email/folders | List mailbox folders
[**list_email_messages**](EmailApi.md#list_email_messages) | **GET** /v1/email/messages | List email messages
[**list_email_threads**](EmailApi.md#list_email_threads) | **GET** /v1/email/threads | List email threads
[**reply_email_message**](EmailApi.md#reply_email_message) | **POST** /v1/email/messages/{messageId}/reply | Reply to a message
[**send_email_message**](EmailApi.md#send_email_message) | **POST** /v1/email/messages | Send an email
[**trash_email_message**](EmailApi.md#trash_email_message) | **DELETE** /v1/email/messages/{messageId} | Move a message to trash
[**update_email_message**](EmailApi.md#update_email_message) | **PATCH** /v1/email/messages/{messageId} | Mark read or starred, or move a message
[**update_email_thread**](EmailApi.md#update_email_thread) | **PATCH** /v1/email/threads/{threadId} | Update every message in a thread



## download_email_attachment

> std::path::PathBuf download_email_attachment(attachment_id, account_id, message_id)
Download an attachment

Streams the attachment bytes with its `Content-Type` and a `Content-Disposition` carrying the filename.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**attachment_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google or Microsoft account. | [required] |
**message_id** | **String** |  | [required] |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/octet-stream, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_email_message

> models::SendEmailMessage201Response get_email_message(message_id, account_id, include_headers, raw)
Get an email message

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google or Microsoft account. | [required] |
**include_headers** | Option<**bool**> | Include the raw internet headers under `headers`. |  |[default to false]
**raw** | Option<**bool**> | Include the MIME source under `raw`. |  |[default to false]

### Return type

[**models::SendEmailMessage201Response**](sendEmailMessage_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_email_thread

> models::GetEmailThread200Response get_email_thread(thread_id, account_id)
Get an email thread with its messages

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**thread_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google or Microsoft account. | [required] |

### Return type

[**models::GetEmailThread200Response**](getEmailThread_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_email_folders

> models::ListEmailFolders200Response list_email_folders(account_id)
List mailbox folders

On Google, folders are Gmail labels (system labels carry `wellKnown`; `unreadCount` and `totalCount` are present only where Gmail reports them). There is no archive folder on Google; archived mail is listed with `folder=archive`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected Google or Microsoft account. | [required] |

### Return type

[**models::ListEmailFolders200Response**](listEmailFolders_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_email_messages

> models::ListEmailMessages200Response list_email_messages(account_id, folder, unread, starred, has_attachment, subject, from, to, cc, bcc, any_email, after, before, search_query_native, sort_order, cursor, limit)
List email messages

Same filters and envelope as `GET /v1/email/threads`, one row per message. Bodies are omitted; fetch a message to read `text` and `html`. On Google, list rows also omit `attachments` (Gmail's metadata pages carry headers only; `hasAttachment=true` still filters server-side), `sortOrder=asc` reverses the fetched page and `archive` means mail without the inbox, trash or spam labels.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected Google or Microsoft account. | [required] |
**folder** | Option<**String**> |  |  |
**unread** | Option<**bool**> |  |  |
**starred** | Option<**bool**> |  |  |
**has_attachment** | Option<**bool**> |  |  |
**subject** | Option<**String**> |  |  |
**from** | Option<**String**> |  |  |
**to** | Option<**String**> |  |  |
**cc** | Option<**String**> |  |  |
**bcc** | Option<**String**> |  |  |
**any_email** | Option<**String**> |  |  |
**after** | Option<**String**> |  |  |
**before** | Option<**String**> |  |  |
**search_query_native** | Option<**String**> |  |  |
**sort_order** | Option<**String**> |  |  |[default to desc]
**cursor** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]

### Return type

[**models::ListEmailMessages200Response**](listEmailMessages_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_email_threads

> models::ListEmailThreads200Response list_email_threads(account_id, folder, unread, starred, has_attachment, subject, from, to, cc, bcc, any_email, after, before, search_query_native, sort_order, cursor, limit)
List email threads

Threads of a connected Google or Microsoft mailbox, newest first. Every filter that the provider cannot apply server-side is applied to the fetched page instead and named in `meta.filteredClientSide`, so a filtered page can hold fewer than `limit` items while `pagination.hasMore` stays true.  On Google, folders are Gmail labels: `folder` takes a well-known name or a label id, `archive` means mail carrying none of the inbox, trash or spam labels, and `sortOrder=asc` reverses the fetched page (Gmail lists newest first only).  The account must have been connected with `scopes=email` (412 `account_scope_missing` otherwise). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected Google or Microsoft account. | [required] |
**folder** | Option<**String**> | Well-known folder (`inbox`, `sent`, `drafts`, `trash`, `spam`, `archive`) or a provider folder id from `GET /v1/email/folders`. Default inbox. |  |
**unread** | Option<**bool**> |  |  |
**starred** | Option<**bool**> |  |  |
**has_attachment** | Option<**bool**> |  |  |
**subject** | Option<**String**> | Substring match on the subject. |  |
**from** | Option<**String**> | Sender address. |  |
**to** | Option<**String**> | A recipient address. |  |
**cc** | Option<**String**> |  |  |
**bcc** | Option<**String**> | Applied client-side on Microsoft. |  |
**any_email** | Option<**String**> | Matches from, to, cc or bcc. Applied client-side on Microsoft. |  |
**after** | Option<**String**> |  |  |
**before** | Option<**String**> |  |  |
**search_query_native** | Option<**String**> | The provider's own search syntax (Gmail search operators, Microsoft KQL). On Microsoft it cannot be combined with other filters or server-side ordering; those are applied to the page. |  |
**sort_order** | Option<**String**> |  |  |[default to desc]
**cursor** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]

### Return type

[**models::ListEmailThreads200Response**](listEmailThreads_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reply_email_message

> models::SendEmailMessage201Response reply_email_message(message_id, reply_email_message_request)
Reply to a message

Replies inside the provider's thread: the provider builds the quoted original and threading headers, your `html` or `text` goes above the quote. `to`, `cc`, `bcc`, `replyTo`, `subject`, `headers` and `attachments` are honoured; `scheduledFor` and `holdAsDraft` are rejected like on send. Same protection, caps and headers as sending.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** |  | [required] |
**reply_email_message_request** | [**ReplyEmailMessageRequest**](ReplyEmailMessageRequest.md) |  | [required] |

### Return type

[**models::SendEmailMessage201Response**](sendEmailMessage_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_email_message

> models::SendEmailMessage201Response send_email_message(send_email_request)
Send an email

Sends from the connected mailbox and returns the stored sent copy. The message is mirrored into the inbox (`message.sent` fires once) and counted against the mailbox's daily cap, reported in the `X-Zernio-Send-Limit`, `X-Zernio-Send-Remaining` and `X-Zernio-Send-Reset` response headers.  Protection on every mailbox: a daily cap (Microsoft 1,000; Google Workspace 500; Gmail consumer 200) that answers 429 `email_send_cap_reached` with `details.cap`; the same body reaching more than 50 distinct recipients within an hour pauses the mailbox with an escalating cooldown (429 `rate_limited`, `account.rate_limited` webhook). These mailboxes are for one-to-one mail, not bulk sends. Gmail sends need a payment method on the workspace (402). Reading, calendar and files do not.  `scheduledFor` and `holdAsDraft` are reserved and currently rejected with 400. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**send_email_request** | [**SendEmailRequest**](SendEmailRequest.md) |  | [required] |

### Return type

[**models::SendEmailMessage201Response**](sendEmailMessage_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## trash_email_message

> models::TrashEmailMessage200Response trash_email_message(message_id, account_id)
Move a message to trash

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google or Microsoft account. | [required] |

### Return type

[**models::TrashEmailMessage200Response**](trashEmailMessage_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_email_message

> models::SendEmailMessage201Response update_email_message(message_id, email_message_patch)
Mark read or starred, or move a message

`folder` moves the message. On Google a move swaps the inbox, trash and spam labels and keeps every other label; `archive` removes the inbox label.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** |  | [required] |
**email_message_patch** | [**EmailMessagePatch**](EmailMessagePatch.md) |  | [required] |

### Return type

[**models::SendEmailMessage201Response**](sendEmailMessage_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_email_thread

> models::UpdateEmailThread200Response update_email_thread(thread_id, email_message_patch)
Update every message in a thread

Applies `unread`, `starred` or a `folder` move to each message of the thread.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**thread_id** | **String** |  | [required] |
**email_message_patch** | [**EmailMessagePatch**](EmailMessagePatch.md) |  | [required] |

### Return type

[**models::UpdateEmailThread200Response**](updateEmailThread_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

