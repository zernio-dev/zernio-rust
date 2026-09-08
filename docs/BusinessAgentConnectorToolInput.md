# BusinessAgentConnectorToolInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**description** | **String** | When and how the agent should use the operation. | 
**request_definition** | **std::collections::HashMap<String, serde_json::Value>** | Meta request definition: method, path, path_parameters, query_parameters, headers and a typed body schema (content_type, params, required). | 
**user_auth_required** | Option<**bool**> |  | [optional]
**user_auth_action_config** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]
**transformation_spec** | Option<**std::collections::HashMap<String, serde_json::Value>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


