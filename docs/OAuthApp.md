# OAuthApp

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Pass it as `oauthAppId` on GET /v1/connect/{platform} to connect through this app. | 
**platform** | **String** | The platform the app belongs to, as in GET /v1/connect/{platform}. | 
**label** | **String** |  | 
**client_id** | **String** | The client ID (or app ID) of your app on the platform. The secret is never returned. | 
**scope_areas** | **Vec<ScopeAreas>** | The permission areas every connect through this app requests. Pick only what your app is approved for on the platform. (enum: posting, analytics, comments, messaging) | 
**status** | **Status** | `ok`: the platform accepted the keys at the last check. `unchecked`: the check could not reach a verdict (see lastError). `invalid`: the platform rejected the keys; connects and token refreshes through this app will fail until the secret is rotated. (enum: ok, unchecked, invalid) | 
**last_checked_at** | Option<**String**> |  | [optional]
**last_error** | Option<**String**> |  | [optional]
**account_count** | **i32** | Connected accounts currently running on this app. | 
**redirect_uri** | **String** | The OAuth redirect URI to allow in your app's settings on the platform. | 
**webhook** | Option<[**models::OAuthAppWebhook**](OAuthAppWebhook.md)> |  | [optional]
**created_at** | **String** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


