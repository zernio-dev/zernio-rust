# TriggerApiCallWorkflowRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**conversation_id** | Option<**String**> | A conversation on the workflow's account | [optional]
**contact_id** | Option<**String**> | A contact with a conversation on the workflow's account | [optional]
**to** | Option<**String**> | Recipient phone in E.164 (WhatsApp workflows only) | [optional]
**variables** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Seed variables, merged over the standard run variables | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


