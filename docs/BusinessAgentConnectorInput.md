# BusinessAgentConnectorInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** | Unique per number. | 
**description** | Option<**String**> | Tell the agent what the service provides. | [optional]
**base_url** | **String** | Public HTTPS URL reachable from Meta. | 
**connector_protocol** | Option<**String**> |  | [optional]
**auth_type** | **AuthType** |  (enum: OAUTH2_CLIENT_CREDENTIALS, API_KEY, NONE) | 
**auth_config** | Option<[**models::BusinessAgentConnectorInputAuthConfig**](BusinessAgentConnectorInputAuthConfig.md)> |  | [optional]
**user_auth_injection_config** | Option<[**models::BusinessAgentConnectorInputUserAuthInjectionConfig**](BusinessAgentConnectorInputUserAuthInjectionConfig.md)> |  | [optional]
**requires_certificate** | Option<**bool**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


