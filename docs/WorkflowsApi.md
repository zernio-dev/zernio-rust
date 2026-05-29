# \WorkflowsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**activate_workflow**](WorkflowsApi.md#activate_workflow) | **POST** /v1/workflows/{workflowId}/activate | Activate workflow
[**create_workflow**](WorkflowsApi.md#create_workflow) | **POST** /v1/workflows | Create workflow
[**delete_workflow**](WorkflowsApi.md#delete_workflow) | **DELETE** /v1/workflows/{workflowId} | Delete workflow
[**get_workflow**](WorkflowsApi.md#get_workflow) | **GET** /v1/workflows/{workflowId} | Get workflow with graph
[**list_workflow_executions**](WorkflowsApi.md#list_workflow_executions) | **GET** /v1/workflows/{workflowId}/executions | List workflow runs
[**list_workflows**](WorkflowsApi.md#list_workflows) | **GET** /v1/workflows | List workflows
[**pause_workflow**](WorkflowsApi.md#pause_workflow) | **POST** /v1/workflows/{workflowId}/pause | Pause workflow
[**trigger_workflow**](WorkflowsApi.md#trigger_workflow) | **POST** /v1/workflows/{workflowId}/executions | Manually start a workflow run
[**update_workflow**](WorkflowsApi.md#update_workflow) | **PATCH** /v1/workflows/{workflowId} | Update workflow



## activate_workflow

> models::ActivateWorkflow200Response activate_workflow(workflow_id)
Activate workflow

Validate the graph is runnable and set the workflow live. Once active, matching inbound messages start executions. Idempotent.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workflow_id** | **String** |  | [required] |

### Return type

[**models::ActivateWorkflow200Response**](activateWorkflow_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_workflow

> models::CreateWorkflow200Response create_workflow(create_workflow_request)
Create workflow

Create a branching conversation workflow (draft) from a node/edge graph. Created in `draft` status; activate it to start matching inbound messages. The graph is validated structurally; completeness (a trigger node + reachable entry) is required at activation. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_workflow_request** | [**CreateWorkflowRequest**](CreateWorkflowRequest.md) |  | [required] |

### Return type

[**models::CreateWorkflow200Response**](createWorkflow_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_workflow

> delete_workflow(workflow_id)
Delete workflow

Permanently delete a workflow and all of its executions.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workflow_id** | **String** |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_workflow

> models::GetWorkflow200Response get_workflow(workflow_id)
Get workflow with graph

Returns a workflow including its full node/edge graph and run stats.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workflow_id** | **String** |  | [required] |

### Return type

[**models::GetWorkflow200Response**](getWorkflow_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_workflow_executions

> models::ListWorkflowExecutions200Response list_workflow_executions(workflow_id, status, limit, skip)
List workflow runs

Returns recent executions (runs) with their status, current node, and accumulated variables.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workflow_id** | **String** |  | [required] |
**status** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 25]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListWorkflowExecutions200Response**](listWorkflowExecutions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_workflows

> models::ListWorkflows200Response list_workflows(profile_id, status, limit, skip)
List workflows

Returns workflows with run stats. Filter by status or profile.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**profile_id** | Option<**String**> | Filter by profile. Omit to list across all profiles |  |
**status** | Option<**String**> |  |  |
**limit** | Option<**i32**> |  |  |[default to 50]
**skip** | Option<**i32**> |  |  |[default to 0]

### Return type

[**models::ListWorkflows200Response**](listWorkflows_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## pause_workflow

> models::PauseWorkflow200Response pause_workflow(workflow_id)
Pause workflow

Stop matching new inbound messages. In-flight executions continue to completion. Idempotent.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workflow_id** | **String** |  | [required] |

### Return type

[**models::PauseWorkflow200Response**](pauseWorkflow_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## trigger_workflow

> models::TriggerWorkflow200Response trigger_workflow(workflow_id, trigger_workflow_request)
Manually start a workflow run

Kick off a run without waiting for an inbound message (useful for testing). Target an existing conversation by `conversationId`, or — WhatsApp only — a phone number via `to` (a conversation is found or created). `text` seeds the run's `lastMessage` variable. The graph must be runnable. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workflow_id** | **String** |  | [required] |
**trigger_workflow_request** | [**TriggerWorkflowRequest**](TriggerWorkflowRequest.md) |  | [required] |

### Return type

[**models::TriggerWorkflow200Response**](triggerWorkflow_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_workflow

> models::UpdateWorkflow200Response update_workflow(workflow_id, update_workflow_request)
Update workflow

Update name, description, or the graph. The graph can only be modified while the workflow is draft or paused.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workflow_id** | **String** |  | [required] |
**update_workflow_request** | Option<[**UpdateWorkflowRequest**](UpdateWorkflowRequest.md)> |  |  |

### Return type

[**models::UpdateWorkflow200Response**](updateWorkflow_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

