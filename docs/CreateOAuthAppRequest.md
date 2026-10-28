# CreateOAuthAppRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **String** | One of the platforms listed in `platforms` of GET /v1/connect/oauth-apps. | 
**label** | **String** |  | 
**client_id** | **String** |  | 
**client_secret** | **String** |  | 
**scope_areas** | Option<**Vec<ScopeAreas>**> | Areas this app requests. Defaults to every area the platform supports; an area the platform cannot request separately is a 400. (enum: posting, analytics, comments, messaging) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


