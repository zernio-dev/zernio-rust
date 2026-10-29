# GetAllAccountsHealth200ResponseAccountsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**username** | Option<**String**> |  | [optional]
**display_name** | Option<**String**> |  | [optional]
**profile_id** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: healthy, warning, error) | [optional]
**can_post** | Option<**bool**> |  | [optional]
**can_fetch_analytics** | Option<**bool**> |  | [optional]
**token_valid** | Option<**bool**> |  | [optional]
**token_expires_at** | Option<**String**> |  | [optional]
**needs_reconnect** | Option<**bool**> | True when the token is expired or revoked, permissions are missing, the account is inactive, or the platform rejected its stored credentials (the same flag the account listing reports as needsReconnection). | [optional]
**issues** | Option<**Vec<String>**> |  | [optional]
**owner_user_id** | Option<**String**> | User id of the profile owner, not necessarily the team member who connected the account. | [optional]
**disconnect_reason** | Option<**String**> | Why the connection is broken or its token refresh is failing, from the most recent current cause. Null when the connection is healthy, including when the account is unhealthy for another reason (analytics, messaging restriction, missing analytics scopes), or when no cause is stored. | [optional]
**disconnection_type** | Option<**DisconnectionType**> | intentional: deliberately disconnected by the user or by Zernio (for example a plan downgrade), not a token failure. unintentional: token expired or revoked, or an auth failure. Null when disconnectReason is null. (enum: intentional, unintentional, ) | [optional]
**unhealthy_since** | Option<**String**> | When the earliest current stored cause was recorded (the start of the outage); for an intentional disconnect, when it was disconnected. Null when the connection is healthy, including when the account is unhealthy for another reason (analytics, messaging restriction, missing analytics scopes), or when the time is unknown. | [optional]
**analytics_sync** | Option<[**models::GetAllAccountsHealth200ResponseAccountsInnerAnalyticsSync**](GetAllAccountsHealth200ResponseAccountsInnerAnalyticsSync.md)> |  | [optional]
**messaging_restriction** | Option<[**models::GetAllAccountsHealth200ResponseAccountsInnerMessagingRestriction**](GetAllAccountsHealth200ResponseAccountsInnerMessagingRestriction.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


