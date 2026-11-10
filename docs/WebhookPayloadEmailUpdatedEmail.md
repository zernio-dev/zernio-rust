# WebhookPayloadEmailUpdatedEmail

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message_id** | Option<**String**> |  | [optional]
**thread_id** | Option<**String**> |  | [optional]
**folder** | Option<**String**> | `inbox`, `sent`, `archive`, `trash`, `spam`, `drafts`, or the provider folder id for any other folder. | [optional]
**unread** | Option<**bool**> |  | [optional]
**starred** | Option<**bool**> | Gmail star or Outlook flag. | [optional]
**labels** | Option<**Vec<String>**> | Gmail user label ids or Outlook category names. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


