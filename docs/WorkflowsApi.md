# \WorkflowsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**activate_workflow**](WorkflowsApi.md#activate_workflow) | **POST** /v1/workflows/{workflowId}/activate | Activate workflow
[**create_workflow**](WorkflowsApi.md#create_workflow) | **POST** /v1/workflows | Create workflow
[**delete_workflow**](WorkflowsApi.md#delete_workflow) | **DELETE** /v1/workflows/{workflowId} | Delete workflow
[**duplicate_workflow**](WorkflowsApi.md#duplicate_workflow) | **POST** /v1/workflows/{workflowId}/duplicate | Duplicate a workflow
[**get_workflow**](WorkflowsApi.md#get_workflow) | **GET** /v1/workflows/{workflowId} | Get workflow with graph
[**get_workflow_version**](WorkflowsApi.md#get_workflow_version) | **GET** /v1/workflows/{workflowId}/versions/{version} | Get a specific workflow version
[**list_workflow_execution_events**](WorkflowsApi.md#list_workflow_execution_events) | **GET** /v1/workflows/{workflowId}/executions/{executionId}/events | Get an execution's timeline
[**list_workflow_executions**](WorkflowsApi.md#list_workflow_executions) | **GET** /v1/workflows/{workflowId}/executions | List workflow runs
[**list_workflow_versions**](WorkflowsApi.md#list_workflow_versions) | **GET** /v1/workflows/{workflowId}/versions | List a workflow's version history
[**list_workflows**](WorkflowsApi.md#list_workflows) | **GET** /v1/workflows | List workflows
[**pause_workflow**](WorkflowsApi.md#pause_workflow) | **POST** /v1/workflows/{workflowId}/pause | Pause workflow
[**restore_workflow_version**](WorkflowsApi.md#restore_workflow_version) | **POST** /v1/workflows/{workflowId}/versions/{version}/restore | Restore a previous workflow version
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


## duplicate_workflow

> models::DuplicateWorkflow201Response duplicate_workflow(workflow_id)
Duplicate a workflow

Create an independent copy of a workflow's graph, name, description, and account binding. The copy is created in `draft` status with fresh execution counters and a new id — execution history is NOT copied. Useful for branching off a known-good workflow before making experimental edits. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workflow_id** | **String** |  | [required] |

### Return type

[**models::DuplicateWorkflow201Response**](duplicateWorkflow_201_response.md)

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


## get_workflow_version

> models::GetWorkflowVersion200Response get_workflow_version(workflow_id, version)
Get a specific workflow version

Returns the full snapshot for a single historical version, including the graph.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workflow_id** | **String** |  | [required] |
**version** | **i32** |  | [required] |

### Return type

[**models::GetWorkflowVersion200Response**](getWorkflowVersion_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_workflow_execution_events

> models::ListWorkflowExecutionEvents200Response list_workflow_execution_events(workflow_id, execution_id)
Get an execution's timeline

Returns the per-step run-log for a single workflow execution: trigger fired, each node visited, edge handles taken, errors, and durations. Backed by Tinybird (90-day retention). Used by the Runs UI drawer to render the timeline. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workflow_id** | **String** |  | [required] |
**execution_id** | **String** |  | [required] |

### Return type

[**models::ListWorkflowExecutionEvents200Response**](listWorkflowExecutionEvents_200_response.md)

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


## list_workflow_versions

> models::ListWorkflowVersions200Response list_workflow_versions(workflow_id)
List a workflow's version history

Returns the snapshot history. A new version is recorded automatically before every PATCH to `nodes` / `edges` / `entryNodeId`, and explicitly when a previous version is restored. Lightweight list — call `getWorkflowVersion` for the full snapshot graph. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workflow_id** | **String** |  | [required] |

### Return type

[**models::ListWorkflowVersions200Response**](listWorkflowVersions_200_response.md)

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


## restore_workflow_version

> models::RestoreWorkflowVersion200Response restore_workflow_version(workflow_id, version)
Restore a previous workflow version

Replace the current graph with the named version's snapshot. Before the swap, the current graph is itself snapshotted as a new version, so a restore is reversible. The workflow must be in `draft` or `paused` status (same gate as a normal graph edit). The returned workflow carries `restoredFromVersion` so the UI can surface which version was rolled back to. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**workflow_id** | **String** |  | [required] |
**version** | **i32** |  | [required] |

### Return type

[**models::RestoreWorkflowVersion200Response**](restoreWorkflowVersion_200_response.md)

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

Update name, description, the graph, or reassign to a different account. The graph can only be modified while the workflow is draft or paused. Account swaps re-validate the graph against the new platform (so e.g. moving from WhatsApp to Facebook surfaces a `start_call` node as an error instead of silently saving an unrunnable graph). 

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

