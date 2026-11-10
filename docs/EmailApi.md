# \EmailApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancel_scheduled_email**](EmailApi.md#cancel_scheduled_email) | **DELETE** /v1/email/messages/scheduled/{scheduleId} | Cancel a scheduled email
[**create_email_label**](EmailApi.md#create_email_label) | **POST** /v1/email/labels | Create a label
[**delete_email_label**](EmailApi.md#delete_email_label) | **DELETE** /v1/email/labels/{labelId} | Delete a label
[**download_email_attachment**](EmailApi.md#download_email_attachment) | **GET** /v1/email/attachments/{attachmentId} | Download an attachment
[**get_email_message**](EmailApi.md#get_email_message) | **GET** /v1/email/messages/{messageId} | Get an email message
[**get_email_thread**](EmailApi.md#get_email_thread) | **GET** /v1/email/threads/{threadId} | Get an email thread with its messages
[**get_scheduled_email**](EmailApi.md#get_scheduled_email) | **GET** /v1/email/messages/scheduled/{scheduleId} | Get a scheduled email
[**list_email_folders**](EmailApi.md#list_email_folders) | **GET** /v1/email/folders | List mailbox folders
[**list_email_labels**](EmailApi.md#list_email_labels) | **GET** /v1/email/labels | List labels
[**list_email_messages**](EmailApi.md#list_email_messages) | **GET** /v1/email/messages | List email messages
[**list_email_threads**](EmailApi.md#list_email_threads) | **GET** /v1/email/threads | List email threads
[**list_scheduled_emails**](EmailApi.md#list_scheduled_emails) | **GET** /v1/email/messages/scheduled | List scheduled emails
[**reply_email_message**](EmailApi.md#reply_email_message) | **POST** /v1/email/messages/{messageId}/reply | Reply to a message
[**send_email_message**](EmailApi.md#send_email_message) | **POST** /v1/email/messages | Send an email
[**trash_email_message**](EmailApi.md#trash_email_message) | **DELETE** /v1/email/messages/{messageId} | Move a message to trash
[**update_email_message**](EmailApi.md#update_email_message) | **PATCH** /v1/email/messages/{messageId} | Mark read or starred, label, or move a message
[**update_email_thread**](EmailApi.md#update_email_thread) | **PATCH** /v1/email/threads/{threadId} | Update every message in a thread



## cancel_scheduled_email

> models::SendEmailMessage202Response cancel_scheduled_email(schedule_id, account_id)
Cancel a scheduled email

Cancels a send still waiting for its time and returns it with `status: cancelled`. One that is sending, sent or failed answers 409.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**schedule_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google or Microsoft account. | [required] |

### Return type

[**models::SendEmailMessage202Response**](sendEmailMessage_202_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_email_label

> models::CreateEmailLabel200Response create_email_label(create_email_label_request)
Create a label

Creates a Gmail label or an Outlook category. Safe to repeat: when the name already exists (case-insensitive) the existing label comes back with 200.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_email_label_request** | [**CreateEmailLabelRequest**](CreateEmailLabelRequest.md) |  | [required] |

### Return type

[**models::CreateEmailLabel200Response**](createEmailLabel_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_email_label

> models::DeleteEmailLabel200Response delete_email_label(label_id, account_id)
Delete a label

Deletes a Gmail user label or an Outlook category, by id or name (URL-encode a slash). Gmail removes the label from every message. Outlook keeps a deleted category on messages that already carry it; 412 when the organization blocks the category list.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**label_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google or Microsoft account. | [required] |

### Return type

[**models::DeleteEmailLabel200Response**](deleteEmailLabel_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


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


## get_scheduled_email

> models::SendEmailMessage202Response get_scheduled_email(schedule_id, account_id)
Get a scheduled email

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**schedule_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google or Microsoft account. | [required] |

### Return type

[**models::SendEmailMessage202Response**](sendEmailMessage_202_response.md)

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


## list_email_labels

> models::ListEmailLabels200Response list_email_labels(account_id)
List labels

Gmail labels, system and user, or the Outlook category list. If an organization blocks reading the Outlook list, it comes back empty and categories still apply to messages by name.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected Google or Microsoft account. | [required] |

### Return type

[**models::ListEmailLabels200Response**](listEmailLabels_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_email_messages

> models::ListEmailMessages200Response list_email_messages(account_id, folder, unread, starred, has_attachment, subject, from, to, cc, bcc, any_email, after, before, search_query_native, sort_order, cursor, limit)
List email messages

Same filters and envelope as `GET /v1/email/threads`, one row per message. Bodies are omitted; fetch a message to read `text` and `html`.  ### On Google  - List rows also omit `attachments` (Gmail's metadata pages carry headers only); `hasAttachment=true` still filters server-side. - `sortOrder=asc` reverses the fetched page. - `archive` means mail without the inbox, trash or spam labels. 

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


## list_scheduled_emails

> models::ListScheduledEmails200Response list_scheduled_emails(account_id, status, cursor, limit)
List scheduled emails

Sends made with `scheduledFor` on this mailbox, in send order. Sent, failed and cancelled ones stay listed; filter with `status`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected Google or Microsoft account. | [required] |
**status** | Option<**String**> |  |  |
**cursor** | Option<**String**> | `pagination.nextCursor` of the previous page. |  |
**limit** | Option<**i32**> |  |  |[default to 50]

### Return type

[**models::ListScheduledEmails200Response**](listScheduledEmails_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reply_email_message

> models::SendEmailMessage201Response reply_email_message(message_id, reply_email_message_request)
Reply to a message

Replies inside the provider's thread: the provider builds the quoted original and threading headers, your `html` or `text` goes above the quote. `to`, `cc`, `bcc`, `replyTo`, `subject`, `headers` and `attachments` are honoured.  `scheduledFor` schedules the reply (202) and `trackOpens`, `trackLinks` and `trackReplies` track it, as on send; `holdAsDraft` holds it as a reply draft in the thread until then. Same protection, caps and headers as sending. 

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

Sends from the connected mailbox and returns the stored sent copy.  The message is mirrored into the inbox (`message.sent` fires once) and counted against the mailbox's daily cap. The cap is reported in the `X-Zernio-Send-Limit`, `X-Zernio-Send-Remaining` and `X-Zernio-Send-Reset` response headers.  ### Sending limits  These mailboxes are for one-to-one mail, not bulk sends. Protection on every mailbox:  - Daily cap: Microsoft 1,000; Google Workspace 500; Gmail consumer 200. Reaching it answers 429 `email_send_cap_reached` with `details.cap`. - The same body reaching more than 50 distinct recipients within an hour pauses the mailbox with an escalating cooldown (429 `rate_limited`, `account.rate_limited` webhook).  ### Scheduling  With `scheduledFor` the request answers 202 with a `ScheduledEmail` instead of sending. The account and payment method are checked now; the caps, cooldowns and the send itself run at `scheduledFor`. A send that fails then fires `email.send_failed`. List, read and cancel scheduled sends under `/v1/email/messages/scheduled`.  ### Tracking  - `trackOpens` adds a 1x1 image to the html and fires `email.opened`. - `trackLinks` rewrites every http(s) link in the html through a Zernio redirect and fires `email.link_clicked`. - `trackReplies` fires `email.thread_replied` when someone else writes in the thread.  Tracking costs nothing extra. Opens are approximate: image proxies prefetch and image blocking hides them.  ### Other errors  - 402: Gmail sends need a payment method on the workspace. Reading, calendar and files do not. - 400: `holdAsDraft` without `scheduledFor`; `trackOpens` or `trackLinks` without `html`; `scheduledFor` outside 1 minute to 30 days. 

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
Mark read or starred, label, or move a message

`addLabels` and `removeLabels` tag the message without moving it. `folder` moves it: on Google a move files the mail in one place, so it drops the inbox, trash, spam and user labels it held; `archive` removes the inbox label.

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

Applies `unread`, `starred`, `addLabels`, `removeLabels` or a `folder` move to each message of the thread.

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

