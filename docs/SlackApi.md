# \SlackApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_slack_members**](SlackApi.md#list_slack_members) | **GET** /v1/accounts/{accountId}/slack-members | List Slack workspace members



## list_slack_members

> models::ListSlackMembers200Response list_slack_members(account_id, query, limit)
List Slack workspace members

Members of the connected Slack workspace that can receive a direct message, for populating a recipient picker. Bots, deactivated members and Slackbot are excluded. Start a DM by passing a member id as `participantId` to POST /v1/inbox/conversations.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** |  | [required] |
**query** | Option<**String**> | Case-insensitive filter over display name and handle. |  |
**limit** | Option<**i32**> |  |  |[default to 50]

### Return type

[**models::ListSlackMembers200Response**](listSlackMembers_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

