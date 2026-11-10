# \EmailApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancel_scheduled_email**](EmailApi.md#cancel_scheduled_email) | **DELETE** /v1/email/messages/scheduled/{scheduleId} | Cancel a scheduled email
[**create_email_draft**](EmailApi.md#create_email_draft) | **POST** /v1/email/drafts | Create a draft
[**create_email_label**](EmailApi.md#create_email_label) | **POST** /v1/email/labels | Create a label
[**create_email_signature**](EmailApi.md#create_email_signature) | **POST** /v1/email/signatures | Create a signature
[**create_imap_account**](EmailApi.md#create_imap_account) | **POST** /v1/email/imap/accounts | Connect an IMAP mailbox
[**declare_email_send_as**](EmailApi.md#declare_email_send_as) | **POST** /v1/email/send-as | Declare a send-as address
[**delete_email_draft**](EmailApi.md#delete_email_draft) | **DELETE** /v1/email/drafts/{draftId} | Delete a draft
[**delete_email_label**](EmailApi.md#delete_email_label) | **DELETE** /v1/email/labels/{labelId} | Delete a label
[**delete_email_send_as**](EmailApi.md#delete_email_send_as) | **DELETE** /v1/email/send-as/{email} | Remove a declared send-as address
[**delete_email_signature**](EmailApi.md#delete_email_signature) | **DELETE** /v1/email/signatures/{signatureId} | Delete a signature
[**discover_imap_settings**](EmailApi.md#discover_imap_settings) | **POST** /v1/email/imap/discover | Find the mail settings for an address
[**download_email_attachment**](EmailApi.md#download_email_attachment) | **GET** /v1/email/attachments/{attachmentId} | Download an attachment
[**forward_email_message**](EmailApi.md#forward_email_message) | **POST** /v1/email/messages/{messageId}/forward | Forward a message
[**get_email_draft**](EmailApi.md#get_email_draft) | **GET** /v1/email/drafts/{draftId} | Get a draft
[**get_email_message**](EmailApi.md#get_email_message) | **GET** /v1/email/messages/{messageId} | Get an email message
[**get_email_signature**](EmailApi.md#get_email_signature) | **GET** /v1/email/signatures/{signatureId} | Get a signature
[**get_email_thread**](EmailApi.md#get_email_thread) | **GET** /v1/email/threads/{threadId} | Get an email thread with its messages
[**get_scheduled_email**](EmailApi.md#get_scheduled_email) | **GET** /v1/email/messages/scheduled/{scheduleId} | Get a scheduled email
[**import_email_signatures**](EmailApi.md#import_email_signatures) | **POST** /v1/email/signatures/import | Import Gmail signatures
[**list_email_drafts**](EmailApi.md#list_email_drafts) | **GET** /v1/email/drafts | List drafts
[**list_email_folders**](EmailApi.md#list_email_folders) | **GET** /v1/email/folders | List mailbox folders
[**list_email_labels**](EmailApi.md#list_email_labels) | **GET** /v1/email/labels | List labels
[**list_email_messages**](EmailApi.md#list_email_messages) | **GET** /v1/email/messages | List email messages
[**list_email_send_as**](EmailApi.md#list_email_send_as) | **GET** /v1/email/send-as | List send-as addresses
[**list_email_signatures**](EmailApi.md#list_email_signatures) | **GET** /v1/email/signatures | List signatures
[**list_email_threads**](EmailApi.md#list_email_threads) | **GET** /v1/email/threads | List email threads
[**list_scheduled_emails**](EmailApi.md#list_scheduled_emails) | **GET** /v1/email/messages/scheduled | List scheduled emails
[**reply_email_message**](EmailApi.md#reply_email_message) | **POST** /v1/email/messages/{messageId}/reply | Reply to a message
[**send_email_draft**](EmailApi.md#send_email_draft) | **POST** /v1/email/drafts/{draftId}/send | Send a draft
[**send_email_message**](EmailApi.md#send_email_message) | **POST** /v1/email/messages | Send an email
[**trash_email_message**](EmailApi.md#trash_email_message) | **DELETE** /v1/email/messages/{messageId} | Move a message to trash
[**update_email_draft**](EmailApi.md#update_email_draft) | **PATCH** /v1/email/drafts/{draftId} | Update a draft
[**update_email_message**](EmailApi.md#update_email_message) | **PATCH** /v1/email/messages/{messageId} | Mark read or starred, label, or move a message
[**update_email_signature**](EmailApi.md#update_email_signature) | **PATCH** /v1/email/signatures/{signatureId} | Update a signature
[**update_email_thread**](EmailApi.md#update_email_thread) | **PATCH** /v1/email/threads/{threadId} | Update every message in a thread



## cancel_scheduled_email

> models::SendEmailMessage202Response cancel_scheduled_email(schedule_id, account_id)
Cancel a scheduled email

Cancels a send still waiting for its time and returns it with `status: cancelled`. One that is sending, sent or failed answers 409.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**schedule_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google, Microsoft or IMAP account. | [required] |

### Return type

[**models::SendEmailMessage202Response**](sendEmailMessage_202_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_email_draft

> models::CreateEmailDraft201Response create_email_draft(create_email_draft_request, idempotency_key)
Create a draft

Saves a draft in the user's mailbox, where they see it in their mail app. Recipients and subject can come later. `inReplyTo` makes a reply draft in that thread and `forwardOf` a forward draft with the original's attachments; the `kind` is fixed for the life of the draft.  Send it with `POST /v1/email/drafts/{draftId}/send`. Edits the user makes in their mail client are what goes out. Store the draft `id`, and pass its `version` as `If-Match` so an update or send applies only to the version you saw. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_email_draft_request** | [**CreateEmailDraftRequest**](CreateEmailDraftRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::CreateEmailDraft201Response**](createEmailDraft_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
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


## create_email_signature

> models::CreateEmailSignature201Response create_email_signature(create_email_signature_request)
Create a signature

Stores a signature Zernio appends on any provider. Without `accountId` it is workspace-wide. `defaultFor` makes it what `appendSignature` uses for those sending addresses. Up to 50 per workspace, 100 KB of html, no scripts.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_email_signature_request** | [**CreateEmailSignatureRequest**](CreateEmailSignatureRequest.md) |  | [required] |

### Return type

[**models::CreateEmailSignature201Response**](createEmailSignature_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_imap_account

> models::ImapConnectResult create_imap_account(create_imap_account_request)
Connect an IMAP mailbox

Connects any IMAP/SMTP mailbox without the hosted page. Email and password are enough when discovery finds the servers. Every check runs before anything is stored; a failure answers 422 with the failing stage's code. An address already on the profile is updated in place and keeps its accountId.  Send `Accept: application/x-ndjson` to stream one line per check as it runs, ending with a `result` line that holds the status and this body.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_imap_account_request** | [**CreateImapAccountRequest**](CreateImapAccountRequest.md) |  | [required] |

### Return type

[**models::ImapConnectResult**](ImapConnectResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## declare_email_send_as

> models::DeclareEmailSendAs200Response declare_email_send_as(declare_email_send_as_request)
Declare a send-as address

Adds an address the provider cannot list, such as an Outlook shared mailbox, so `from` accepts it. It starts `unverified` and becomes `accepted` after its first send. Gmail answers 400: add aliases in Gmail settings instead. An address already listed comes back with 200.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**declare_email_send_as_request** | [**DeclareEmailSendAsRequest**](DeclareEmailSendAsRequest.md) |  | [required] |

### Return type

[**models::DeclareEmailSendAs200Response**](declareEmailSendAs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_email_draft

> models::DeleteEmailDraft200Response delete_email_draft(draft_id, account_id)
Delete a draft

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**draft_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google, Microsoft or IMAP account. | [required] |

### Return type

[**models::DeleteEmailDraft200Response**](deleteEmailDraft_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_email_label

> models::DeleteEmailDraft200Response delete_email_label(label_id, account_id)
Delete a label

Deletes a Gmail user label or an Outlook category, by id or name (URL-encode a slash). Gmail removes the label from every message. Outlook keeps a deleted category on messages that already carry it; 412 when the organization blocks the category list.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**label_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google, Microsoft or IMAP account. | [required] |

### Return type

[**models::DeleteEmailDraft200Response**](deleteEmailDraft_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_email_send_as

> models::DeleteEmailSendAs200Response delete_email_send_as(email, account_id)
Remove a declared send-as address

Removes an address declared with `POST /v1/email/send-as`. Addresses the provider lists cannot be removed here. URL-encode the `@`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**email** | **String** |  | [required] |
**account_id** | **String** | The connected Google, Microsoft or IMAP account. | [required] |

### Return type

[**models::DeleteEmailSendAs200Response**](deleteEmailSendAs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_email_signature

> models::DeleteEmailDraft200Response delete_email_signature(signature_id)
Delete a signature

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**signature_id** | **String** |  | [required] |

### Return type

[**models::DeleteEmailDraft200Response**](deleteEmailDraft_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## discover_imap_settings

> models::DiscoverImapSettings200Response discover_imap_settings(discover_imap_settings_request)
Find the mail settings for an address

The routing decision the hosted page makes, for your own connect form: Google or Microsoft OAuth, IMAP with the servers and the provider's app-password steps, or unsupported. Sources run in parallel inside 15 seconds: presets, MX, autoconfig, Thunderbird's ISPDB (sent the domain only), SRV records, then a probe.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**discover_imap_settings_request** | [**DiscoverImapSettingsRequest**](DiscoverImapSettingsRequest.md) |  | [required] |

### Return type

[**models::DiscoverImapSettings200Response**](discoverImapSettings_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
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
**account_id** | **String** | The connected Google, Microsoft or IMAP account. | [required] |
**message_id** | **String** |  | [required] |

### Return type

[**std::path::PathBuf**](std::path::PathBuf.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/octet-stream, application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## forward_email_message

> models::SendEmailMessage201Response forward_email_message(message_id, forward_email_request, idempotency_key)
Forward a message

Forwards the message with its attachments. Your `text` or `html` goes above the forwarded mail, and the subject defaults to \"Fwd: \" plus the original's. On Google the forward stays in the original thread; on Microsoft it goes through Outlook's own forward.  `includeAttachments: false` keeps only the original's inline images, and `excludeAttachmentIds` leaves out the ones you name. Everything together stays under 25 MB.  `trackOpens`, `trackLinks` and `trackReplies` work as on send. Same protection, caps and headers as sending. The response carries `forwardedFrom`, and `email.sent` fires with `source: forward`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** |  | [required] |
**forward_email_request** | [**ForwardEmailRequest**](ForwardEmailRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::SendEmailMessage201Response**](sendEmailMessage_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_email_draft

> models::CreateEmailDraft201Response get_email_draft(draft_id, account_id)
Get a draft

The draft as it stands in the mailbox now, with its bodies. A draft deleted in the mail client answers 404.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**draft_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google, Microsoft or IMAP account. | [required] |

### Return type

[**models::CreateEmailDraft201Response**](createEmailDraft_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_email_message

> models::SendEmailMessage201Response get_email_message(message_id, account_id, include_headers, raw, clean)
Get an email message

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google, Microsoft or IMAP account. | [required] |
**include_headers** | Option<**bool**> | Include the raw internet headers under `headers`. |  |[default to false]
**raw** | Option<**bool**> | Include the MIME source under `raw`. |  |[default to false]
**clean** | Option<**bool**> | Add a `clean` object: the new text without quoted replies, footers or tracking pixels, the `signature` on its own (it also stays in `text`), and a parsed `forwarded` header. Ready to hand to an LLM. |  |[default to false]

### Return type

[**models::SendEmailMessage201Response**](sendEmailMessage_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_email_signature

> models::CreateEmailSignature201Response get_email_signature(signature_id)
Get a signature

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**signature_id** | **String** |  | [required] |

### Return type

[**models::CreateEmailSignature201Response**](createEmailSignature_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_email_thread

> models::GetEmailThread200Response get_email_thread(thread_id, account_id, clean)
Get an email thread with its messages

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**thread_id** | **String** |  | [required] |
**account_id** | **String** | The connected Google, Microsoft or IMAP account. | [required] |
**clean** | Option<**bool**> | Add a `clean` object to every message: the text each one added, without quoted replies, footers or tracking pixels, plus its `signature` and a parsed `forwarded` header. |  |[default to false]

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
**account_id** | **String** | The connected Google, Microsoft or IMAP account. | [required] |

### Return type

[**models::SendEmailMessage202Response**](sendEmailMessage_202_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## import_email_signatures

> models::ListEmailSignatures200Response import_email_signatures(account_id)
Import Gmail signatures

Copies each Gmail send-as signature into a Zernio signature on that account, the default for its address. Repeating it refreshes the copies. Outlook answers 400: Microsoft Graph does not expose signatures.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected Google, Microsoft or IMAP account. | [required] |

### Return type

[**models::ListEmailSignatures200Response**](listEmailSignatures_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_email_drafts

> models::ListEmailDrafts200Response list_email_drafts(account_id, limit, cursor)
List drafts

The mailbox's drafts, newest first, including drafts the user wrote in their mail app. Drafts in the trash are left out. Rows carry no bodies on Google; get a draft to read them.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected Google, Microsoft or IMAP account. | [required] |
**limit** | Option<**i32**> |  |  |[default to 25]
**cursor** | Option<**String**> |  |  |

### Return type

[**models::ListEmailDrafts200Response**](listEmailDrafts_200_response.md)

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
**account_id** | **String** | The connected Google, Microsoft or IMAP account. | [required] |

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
**account_id** | **String** | The connected Google, Microsoft or IMAP account. | [required] |

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
**account_id** | **String** | The connected Google, Microsoft or IMAP account. | [required] |
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


## list_email_send_as

> models::ListEmailSendAs200Response list_email_send_as(account_id)
List send-as addresses

The addresses a mailbox can send from, for `from`, each with the signature `appendSignature` would add. Gmail lists every alias itself. Outlook lists the mailbox address and its aliases, plus any address declared with `POST /v1/email/send-as`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected Google, Microsoft or IMAP account. | [required] |

### Return type

[**models::ListEmailSendAs200Response**](listEmailSendAs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_email_signatures

> models::ListEmailSignatures200Response list_email_signatures(account_id)
List signatures

Zernio-stored signatures: workspace-wide ones plus those of the accounts you can see. With `accountId`, only workspace-wide ones and that account's.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | Option<**String**> |  |  |

### Return type

[**models::ListEmailSignatures200Response**](listEmailSignatures_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_email_threads

> models::ListEmailThreads200Response list_email_threads(account_id, folder, unread, starred, has_attachment, subject, from, to, cc, bcc, any_email, after, before, search_query_native, sort_order, cursor, limit)
List email threads

Threads of a connected Google, Microsoft or IMAP mailbox, newest first. Every filter that the provider cannot apply server-side is applied to the fetched page instead and named in `meta.filteredClientSide`, so a filtered page can hold fewer than `limit` items while `pagination.hasMore` stays true.  On Google, folders are Gmail labels: `folder` takes a well-known name or a label id, `archive` means mail carrying none of the inbox, trash or spam labels, and `sortOrder=asc` reverses the fetched page (Gmail lists newest first only).  The account must have been connected with `scopes=email` (412 `account_scope_missing` otherwise). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | The connected Google, Microsoft or IMAP account. | [required] |
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
**account_id** | **String** | The connected Google, Microsoft or IMAP account. | [required] |
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

> models::SendEmailMessage201Response reply_email_message(message_id, reply_email_message_request, idempotency_key)
Reply to a message

Replies inside the provider's thread: the provider builds the quoted original and threading headers, your `html` or `text` goes above the quote. `to`, `cc`, `bcc`, `replyTo`, `subject`, `headers` and `attachments` are honoured.  `scheduledFor` schedules the reply (202) and `trackOpens`, `trackLinks` and `trackReplies` track it, as on send; `holdAsDraft` holds it as a reply draft in the thread until then. Same protection, caps and headers as sending. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**message_id** | **String** |  | [required] |
**reply_email_message_request** | [**ReplyEmailMessageRequest**](ReplyEmailMessageRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::SendEmailMessage201Response**](sendEmailMessage_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_email_draft

> models::SendEmailMessage201Response send_email_draft(draft_id, send_email_draft_request, if_match, idempotency_key)
Send a draft

Sends the draft as it stands in the mailbox now, edits made in their mail app included, and returns the sent message with `draftId`. The draft needs at least one recipient. A draft the user deleted or already sent answers 404 `draft_not_found`.  With `If-Match` it goes out only if it is still the version the approver saw (412 `draft_conflict` otherwise). If the user removed the open pixel or rewrote links, tracking is put back before it is sent. Fires `email.sent` with `source: draft`.  Tracking set when the draft was created applies, and its `metadata` comes back on the sent message. Same protection, caps and headers as sending. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**draft_id** | **String** |  | [required] |
**send_email_draft_request** | [**SendEmailDraftRequest**](SendEmailDraftRequest.md) |  | [required] |
**if_match** | Option<**String**> | The draft `version` (also its `ETag`). The request applies only if the draft is still that version; otherwise 412 `draft_conflict` with the current draft in `details.draft`. |  |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

### Return type

[**models::SendEmailMessage201Response**](sendEmailMessage_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## send_email_message

> models::SendEmailMessage201Response send_email_message(send_email_request, idempotency_key)
Send an email

Sends from the connected mailbox and returns the stored sent copy.  The message is mirrored into the inbox (`message.sent` fires once) and counted against the mailbox's daily cap. The cap is reported in the `X-Zernio-Send-Limit`, `X-Zernio-Send-Remaining` and `X-Zernio-Send-Reset` response headers.  ### Sending limits  These mailboxes are for one-to-one mail, not bulk sends. Protection on every mailbox:  - Daily cap: Microsoft 1,000; Google Workspace 500; Gmail consumer 200. Reaching it answers 429 `email_send_cap_reached` with `details.cap`. - The same body reaching more than 50 distinct recipients within an hour pauses the mailbox with an escalating cooldown (429 `rate_limited`, `account.rate_limited` webhook).  ### Scheduling  With `scheduledFor` the request answers 202 with a `ScheduledEmail` instead of sending. The account and payment method are checked now; the caps, cooldowns and the send itself run at `scheduledFor`. A send that fails then fires `email.send_failed`. List, read and cancel scheduled sends under `/v1/email/messages/scheduled`.  ### Tracking  - `trackOpens` adds a 1x1 image to the html and fires `email.opened`. - `trackLinks` rewrites every http(s) link in the html through a Zernio redirect and fires `email.link_clicked`. - `trackReplies` fires `email.thread_replied` when someone else writes in the thread.  Tracking costs nothing extra. Opens are approximate: image proxies prefetch and image blocking hides them.  ### Other errors  - 402: Gmail sends need a payment method on the workspace. Reading, calendar and files do not. - 400: `holdAsDraft` without `scheduledFor`; `trackOpens` or `trackLinks` without `html`; `scheduledFor` outside 1 minute to 30 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**send_email_request** | [**SendEmailRequest**](SendEmailRequest.md) |  | [required] |
**idempotency_key** | Option<**String**> | Optional client-generated unique key (e.g. a UUID) that makes retries safe.  - Same key + same body: replays the original response. - Same key + different body: 422. - Key still processing: 409.  A request cut off mid-handler (e.g. by a function timeout) can leave its key in progress, answering 409 until the key expires after 24 hours.  On the Ads create, boost and duplicate endpoints, a same-body retry runs again once the cut-off request started more than 15 minutes ago.  |  |

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
**account_id** | **String** | The connected Google, Microsoft or IMAP account. | [required] |

### Return type

[**models::TrashEmailMessage200Response**](trashEmailMessage_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_email_draft

> models::CreateEmailDraft201Response update_email_draft(draft_id, update_email_draft_request, if_match)
Update a draft

Changes the fields you send and keeps the rest. A reply draft stays in its thread, and a new body on a reply or forward draft goes above the quoted original. With `If-Match`, a draft someone edited since answers 412 `draft_conflict` with the current draft.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**draft_id** | **String** |  | [required] |
**update_email_draft_request** | [**UpdateEmailDraftRequest**](UpdateEmailDraftRequest.md) |  | [required] |
**if_match** | Option<**String**> | The draft `version` (also its `ETag`). The request applies only if the draft is still that version; otherwise 412 `draft_conflict` with the current draft in `details.draft`. |  |

### Return type

[**models::CreateEmailDraft201Response**](createEmailDraft_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
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


## update_email_signature

> models::CreateEmailSignature201Response update_email_signature(signature_id, update_email_signature_request)
Update a signature

Changes the name, html, text or `defaultFor`. Taking an address in `defaultFor` removes it from the other signatures of the same scope.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**signature_id** | **String** |  | [required] |
**update_email_signature_request** | [**UpdateEmailSignatureRequest**](UpdateEmailSignatureRequest.md) |  | [required] |

### Return type

[**models::CreateEmailSignature201Response**](createEmailSignature_201_response.md)

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

