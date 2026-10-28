# WebhookPayloadAccountPermissionsChangedAccount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**profile_id** | **String** |  | 
**platform** | **String** |  | 
**username** | **String** |  | 
**display_name** | Option<**String**> |  | [optional]
**oauth_app_id** | **String** | The OAuth app the account connected through. | 
**missing_scope_areas** | **Vec<MissingScopeAreas>** | Every area now missing. Enable the permission on your app (or have the user grant it), then reconnect the account. (enum: posting, analytics, comments, messaging) | 
**reason** | **String** | The platform error that revealed it. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


