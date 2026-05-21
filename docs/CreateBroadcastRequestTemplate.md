# CreateBroadcastRequestTemplate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**language** | Option<**String**> |  | [optional]
**components** | Option<**Vec<serde_json::Value>**> |  | [optional]
**variable_mapping** | Option<[**std::collections::HashMap<String, models::CreateBroadcastRequestTemplateVariableMappingValue>**](CreateBroadcastRequestTemplateVariableMappingValue.md)> | Maps template variable positions (\"1\", \"2\") to contact fields or static values. Resolved per recipient at send time. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


