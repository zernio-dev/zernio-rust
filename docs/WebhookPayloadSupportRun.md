# WebhookPayloadSupportRun

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**test** | Option<**bool**> | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional]
**id** | **String** | Event id, the dedupe key. | 
**event** | **Event** |  (enum: support.run.completed, support.run.failed) | 
**timestamp** | **String** |  | 
**run** | [**models::SupportRun**](SupportRun.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


