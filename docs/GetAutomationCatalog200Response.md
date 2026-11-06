# GetAutomationCatalog200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**schema** | **serde_json::Value** | JSON Schema of the body of `POST /v1/automations`. | 
**triggers** | [**Vec<models::GetAutomationCatalog200ResponseTriggersInner>**](GetAutomationCatalog200ResponseTriggersInner.md) |  | 
**subjects** | [**Vec<models::GetAutomationCatalog200ResponseSubjectsInner>**](GetAutomationCatalog200ResponseSubjectsInner.md) | Ad rule subjects. | 
**filters** | **serde_json::Value** | The fields and operators `subjects.filters` takes, and which fields each subject accepts. | 
**groups** | **serde_json::Value** | What `subjects.groups` takes. | 
**alert** | **serde_json::Value** | The most checks `alert.confirmChecks` can ask for. | 
**conditions** | **serde_json::Value** | Condition operators, windows, `compareTo` options and size limits. | 
**limits** | **Vec<String>** |  | 
**approval** | **serde_json::Value** | Where `approval.request` goes, how many approvers and how long it can wait. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


