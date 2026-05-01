# \CommentAutomationsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_comment_automation**](CommentAutomationsApi.md#create_comment_automation) | **POST** /v1/comment-automations | Create comment-to-DM automation
[**delete_comment_automation**](CommentAutomationsApi.md#delete_comment_automation) | **DELETE** /v1/comment-automations/{automationId} | Delete automation
[**get_comment_automation**](CommentAutomationsApi.md#get_comment_automation) | **GET** /v1/comment-automations/{automationId} | Get automation details
[**list_comment_automation_logs**](CommentAutomationsApi.md#list_comment_automation_logs) | **GET** /v1/comment-automations/{automationId}/logs | List automation logs
[**list_comment_automations**](CommentAutomationsApi.md#list_comment_automations) | **GET** /v1/comment-automations | List comment-to-DM automations
[**update_comment_automation**](CommentAutomationsApi.md#update_comment_automation) | **PATCH** /v1/comment-automations/{automationId} | Update automation settings



## create_comment_automation

> models::CreateCommentAutomation200Response create_comment_automation(create_comment_automation_request)
Create comment-to-DM automation

Create a keyword-triggered DM automation on an Instagram or Facebook account. When someone comments a matching keyword, they automatically receive a DM.  Two modes:   * **Per-post** — set `platformPostId` to scope the automation to one specific post.     Only one active per-post automation is allowed per post.   * **Account-wide (\"any post\")** — omit `platformPostId` (and `postId`). The automation     evaluates every comment on every post on the account. You can stack unlimited     account-wide automations, each with its own keyword set, and they all run     independently. Per-post automations take priority on their post. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_comment_automation_request** | [**CreateCommentAutomationRequest**](CreateCommentAutomationRequest.md) |  | [required] |

### Return type

[**models::CreateCommentAutomation200Response**](createCommentAutomation_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_comment_automation

> delete_comment_automation(automation_id)
Delete automation

Permanently delete an automation and all its trigger logs.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_comment_automation

> models::GetCommentAutomation200Response get_comment_automation(automation_id)
Get automation details

Returns an automation with its configuration, stats, and recent trigger logs.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |

### Return type

[**models::GetCommentAutomation200Response**](getCommentAutomation_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_comment_automation_logs

> models::ListCommentAutomationLogs200Response list_comment_automation_logs(automation_id, status, limit, skip)
List automation logs

Paginated list of every comment that triggered this automation, with send status and commenter info.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |
**status** | Option<**String**> | Filter by result status |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListCommentAutomationLogs200Response**](listCommentAutomationLogs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_comment_automations

> models::ListCommentAutomations200Response list_comment_automations(profile_id)
List comment-to-DM automations

List all comment-to-DM automations for a profile. Returns automations with their stats.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> | Filter by profile. Omit to list across all profiles |  |

### Return type

[**models::ListCommentAutomations200Response**](listCommentAutomations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_comment_automation

> models::UpdateCommentAutomation200Response update_comment_automation(automation_id, update_comment_automation_request)
Update automation settings

Update an automation's keywords, DM message, comment reply, or active status.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**automation_id** | **String** |  | [required] |
**update_comment_automation_request** | Option<[**UpdateCommentAutomationRequest**](UpdateCommentAutomationRequest.md)> |  |  |

### Return type

[**models::UpdateCommentAutomation200Response**](updateCommentAutomation_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

