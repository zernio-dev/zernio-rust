# \MentionsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_inbox_mentions**](MentionsApi.md#list_inbox_mentions) | **GET** /v1/inbox/mentions | List mentions



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

