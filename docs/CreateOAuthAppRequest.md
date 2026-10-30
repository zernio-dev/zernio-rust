# CreateOAuthAppRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **String** | One of the platforms listed in `platforms` of GET /v1/connect/oauth-apps. | 
**label** | **String** |  | 
**client_id** | **String** |  | 
**client_secret** | **String** |  | 
**meta_app_id** | Option<**String**> | Instagram only: the numeric ID of the Meta app your Instagram app lives in. Zernio uses it with `metaAppSecret` to register the webhook. Send both or neither. | [optional]
**meta_app_secret** | Option<**String**> | Instagram only: the secret of that Meta app. Never returned. | [optional]
**slack_signing_secret** | Option<**String**> | Slack only: the signing secret from the app's Basic Information page. Needed to receive events from your Slack app; any other platform is a 400. | [optional]
**scope_areas** | Option<**Vec<ScopeAreas>**> | Areas this app requests. Defaults to every area the platform supports; an area the platform cannot request separately is a 400. (enum: posting, analytics, comments, messaging) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


