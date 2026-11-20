# \WorkspacesApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_workspace**](WorkspacesApi.md#create_workspace) | **POST** /v1/workspaces | Create workspace
[**create_workspace_api_key**](WorkspacesApi.md#create_workspace_api_key) | **POST** /v1/workspaces/{workspaceId}/api-keys | Create workspace key
[**delete_workspace**](WorkspacesApi.md#delete_workspace) | **DELETE** /v1/workspaces/{workspaceId} | Delete workspace
[**get_workspace**](WorkspacesApi.md#get_workspace) | **GET** /v1/workspaces/{workspaceId} | Get workspace
[**list_workspaces**](WorkspacesApi.md#list_workspaces) | **GET** /v1/workspaces | List workspaces
[**update_workspace**](WorkspacesApi.md#update_workspace) | **PATCH** /v1/workspaces/{workspaceId} | Rename workspace



## create_workspace

> models::CreateWorkspace201Response create_workspace(create_workspace_request)
Create workspace

Creates a new, empty workspace owned by the key's owner, for example one per client of your product.  - Send `apiKey` to get the new workspace's first key in the same call. A key only manages its own workspace, so no other key can mint one there later. - The workspace has no billing. Its keys can read, but writes return 402 `workspace_billing_required` until billing is set up at `billing.setupUrl`. - Needs a full-access key. Creation is capped at 5 a day and 20 owned workspaces without billing (429). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_workspace_request** | [**CreateWorkspaceRequest**](CreateWorkspaceRequest.md) |  | [required] |

### Return type

[**models::CreateWorkspace201Response**](createWorkspace_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_workspace_api_key

> models::CreateWorkspaceApiKey201Response create_workspace_api_key(workspace_id, create_workspace_api_key_request)
Create workspace key

Creates another API key that acts in this workspace as its creator. It covers every profile, and its full value is returned only once.  - The caller must be owner or admin there. - The calling credential must be a full-access key of this same workspace. Profile-scoped, restricted and handed-over keys, OAuth tokens and keys of other workspaces get 403. - For another workspace, use the dashboard. For a new one, send `apiKey` on `POST /v1/workspaces`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | **String** |  | [required] |
**create_workspace_api_key_request** | [**CreateWorkspaceApiKeyRequest**](CreateWorkspaceApiKeyRequest.md) |  | [required] |

### Return type

[**models::CreateWorkspaceApiKey201Response**](createWorkspaceApiKey_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_workspace

> models::GetWorkspace200Response delete_workspace(workspace_id, move_balance_to, forfeit_balance)
Delete workspace

Schedules the workspace for deletion 48 hours ahead, as the dashboard does. Members keep working, publishing is paused, and the owner or an admin can cancel from the dashboard until then. Only this workspace's data is deleted, never its members' accounts.  - Owner only, with a full-access key of this workspace. A key of another workspace gets 403; delete it from the dashboard. - A Personal workspace is never deleted. - Refused while the workspace owes a payment or holds a phone number or carrier registration (409 `deletion_blocked`). - With a balance above $0, send `moveBalanceTo` (another billed workspace you own) or `forfeitBalance=true`. Balances are never refunded. Without either the call returns 422 `deletion_balance_choice`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | **String** |  | [required] |
**move_balance_to** | Option<**String**> | A billed workspace you own that receives the remaining balance. |  |
**forfeit_balance** | Option<**bool**> | Leave the remaining balance; it is written off when the workspace is deleted. |  |

### Return type

[**models::GetWorkspace200Response**](getWorkspace_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_workspace

> models::GetWorkspace200Response get_workspace(workspace_id)
Get workspace

Returns one workspace the key's owner belongs to, with their role. Owners, admins and billing admins also get `billing` (whether it is set up, and where to set it up); members and viewers do not.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | **String** |  | [required] |

### Return type

[**models::GetWorkspace200Response**](getWorkspace_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_workspaces

> models::ListWorkspaces200Response list_workspaces(limit, skip)
List workspaces

Lists every workspace the key's owner belongs to, with their role in each: teams first by name, their Personal workspace last. Any key of the owner lists them all, whatever workspace that key acts in.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**limit** | Option<**i32**> | Page size. |  |[default to 50]
**skip** | Option<**i32**> | Number of workspaces to skip. |  |[default to 0]

### Return type

[**models::ListWorkspaces200Response**](listWorkspaces_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_workspace

> models::GetWorkspace200Response update_workspace(workspace_id, update_workspace_request)
Rename workspace

Renames a workspace. Owner or admin there, with a full-access key of this workspace (a key of another workspace gets 403: rename it from the dashboard). Only a Personal workspace can be called \"Personal\".

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workspace_id** | **String** |  | [required] |
**update_workspace_request** | [**UpdateWorkspaceRequest**](UpdateWorkspaceRequest.md) |  | [required] |

### Return type

[**models::GetWorkspace200Response**](getWorkspace_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

