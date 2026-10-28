# OAuthAppSetup

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **String** |  | 
**redirect_uri** | **String** | Allow this OAuth redirect URI in your app on the platform. | 
**core_scopes** | **Vec<String>** | Requested on every connect, whatever areas the app enables. | 
**scope_areas** | [**Vec<models::OAuthAppSetupScopeAreasInner>**](OAuthAppSetupScopeAreasInner.md) | The areas an app on this platform can enable, each with the scopes it requests. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


