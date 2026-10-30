# UpdateOAuthAppRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**label** | Option<**String**> |  | [optional]
**client_secret** | Option<**String**> |  | [optional]
**meta_app_id** | Option<**String**> | Instagram only: the numeric ID of the Meta app your Instagram app lives in. Zernio uses it with `metaAppSecret` to register the webhook. Send both or neither. | [optional]
**meta_app_secret** | Option<**String**> | Instagram only: the secret of that Meta app. Never returned. | [optional]
**slack_signing_secret** | Option<**String**> | Slack only: saves or replaces the signing secret from the app's Basic Information page; any other platform is a 400. | [optional]
**scope_areas** | Option<**Vec<ScopeAreas>**> | Replaces the areas new connects request. Accounts already connected keep what they were granted until they reconnect. (enum: posting, analytics, comments, messaging) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


