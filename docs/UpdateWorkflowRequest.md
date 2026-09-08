# UpdateWorkflowRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**description** | Option<**String**> |  | [optional]
**nodes** | Option<[**Vec<models::WorkflowNode>**](WorkflowNode.md)> |  | [optional]
**edges** | Option<[**Vec<models::WorkflowEdge>**](WorkflowEdge.md)> |  | [optional]
**entry_node_id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> | Reassign the workflow to a different `SocialAccount`. `platform` and `profileId` are derived server-side from the new account (the client never sends them directly). The account must belong to the caller's team and be on a workflow-supported platform (whatsapp, instagram, facebook, telegram, twitter, bluesky, reddit). Changing this triggers a graph revalidation against the new platform.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


