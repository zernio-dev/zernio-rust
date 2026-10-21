# UpdateConnectWelcomeScreenRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**show_by_default** | **bool** | Show the welcome screen on connect calls that do not pass `welcome`. | 
**brand_name** | Option<**String**> |  | [optional]
**logo_url** | Option<**String**> | https URL of a square logo. | [optional]
**theme** | Option<**serde_json::Value**> | Same keys as the `welcomeTheme` parameter of `GET /v1/connect/{platform}`, as a JSON object. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


