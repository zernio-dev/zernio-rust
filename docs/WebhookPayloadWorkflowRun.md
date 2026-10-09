# WebhookPayloadWorkflowRun

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**test** | Option<**bool**> | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional]
**id** | **String** | Event id, the dedupe key. | 
**event** | **Event** |  (enum: workflow.run.started, workflow.run.completed, workflow.run.failed) | 
**timestamp** | **String** |  | 
**workflow** | [**models::WebhookPayloadWorkflowRunWorkflow**](WebhookPayloadWorkflowRunWorkflow.md) |  | 
**execution** | [**models::WebhookPayloadWorkflowRunExecution**](WebhookPayloadWorkflowRunExecution.md) |  | 
**conversation** | [**models::WebhookPayloadWorkflowRunConversation**](WebhookPayloadWorkflowRunConversation.md) |  | 
**contact** | [**models::WebhookPayloadContactTagContact**](WebhookPayloadContactTagContact.md) |  | 
**trigger** | [**models::WebhookPayloadWorkflowRunTrigger**](WebhookPayloadWorkflowRunTrigger.md) |  | 
**error** | Option<**String**> | workflow.run.failed only: which node failed and why. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


