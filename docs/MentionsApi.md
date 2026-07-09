# \MentionsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_inbox_mentions**](MentionsApi.md#list_inbox_mentions) | **GET** /v1/inbox/mentions | List mentions
[**reply_to_mention**](MentionsApi.md#reply_to_mention) | **POST** /v1/inbox/mentions/reply | Reply to a mention



## list_inbox_mentions

> models::ListInboxMentions200Response list_inbox_mentions(account_id, profile_id, sort_order, limit, cursor)
List mentions

Returns mentions of your connected organization accounts, delivered via platform webhooks. Currently supports LinkedIn organization mentions.  Requires Inbox addon. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | Option<**String**> | Filter by social account ID |  |
**profile_id** | Option<**String**> | Filter by profile ID |  |
**sort_order** | Option<**String**> | Sort order by publishedAt |  |[default to desc]
**limit** | Option<**i32**> |  |  |[default to 25]
**cursor** | Option<**String**> | Cursor for pagination (ID of the last item from the previous page) |  |

### Return type

[**models::ListInboxMentions200Response**](listInboxMentions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reply_to_mention

> models::ReplyToMention200Response reply_to_mention(reply_to_mention_request)
Reply to a mention

Reply to a mention of the connected account. Supported on Instagram only.  Two shapes, selected by whether `commentId` is present:  - **Comment mention** (someone @mentioned the account inside a comment): pass both   `mediaId` and `commentId`. Instagram posts a reply under that comment. - **Caption mention** (someone @mentioned the account in their media caption, so no   comment exists): pass `mediaId` only. Instagram posts a comment on their media.  Story mentions are not supported by Instagram's API.  Note that `GET /v1/inbox/mentions` currently returns LinkedIn mentions only and does not surface Instagram mentions. Source `mediaId` and `commentId` from Instagram's `comments` webhook, which is where mention notifications are delivered for accounts connected through Instagram Login. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**reply_to_mention_request** | [**ReplyToMentionRequest**](ReplyToMentionRequest.md) |  | [required] |

### Return type

[**models::ReplyToMention200Response**](replyToMention_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

