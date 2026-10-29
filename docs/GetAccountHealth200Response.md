# GetAccountHealth200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**integration_lane** | Option<**IntegrationLane**> | TikTok only. The TikTok integration the account is connected through: business (TikTok for Business, Accounts API) or developer (the original integration). Absent on other platforms. (enum: business, developer) | [optional]
**send_cap** | Option<[**models::GetAccountHealth200ResponseSendCap**](GetAccountHealth200ResponseSendCap.md)> |  | [optional]
**push** | Option<**Push**> | Google and Microsoft only: state of the provider change-notification subscriptions behind `message.received` and `calendar.event.*`. `pending` means a granted area has no live subscription yet (retried every 6 hours), `failed` that renewals keep failing (reconnect the account). (enum: active, pending, failed, not_applicable) | [optional]
**username** | Option<**String**> |  | [optional]
**display_name** | Option<**String**> |  | [optional]
**status** | Option<**Status**> | Overall health status (enum: healthy, warning, error) | [optional]
**token_status** | Option<[**models::GetAccountHealth200ResponseTokenStatus**](GetAccountHealth200ResponseTokenStatus.md)> |  | [optional]
**permissions** | Option<[**models::GetAccountHealth200ResponsePermissions**](GetAccountHealth200ResponsePermissions.md)> |  | [optional]
**issues** | Option<**Vec<String>**> | List of issues found | [optional]
**recommendations** | Option<**Vec<String>**> | Actionable recommendations to fix issues | [optional]
**owner_user_id** | Option<**String**> | User id of the profile owner, not necessarily the team member who connected the account. | [optional]
**disconnect_reason** | Option<**String**> | Why the connection is broken or its token refresh is failing, from the most recent current cause. Null when the connection is healthy, including when the account is unhealthy for another reason (analytics, messaging restriction, missing analytics scopes), or when no cause is stored. | [optional]
**disconnection_type** | Option<**DisconnectionType**> | intentional: deliberately disconnected by the user or by Zernio (for example a plan downgrade), not a token failure. unintentional: token expired or revoked, or an auth failure. Null when disconnectReason is null. (enum: intentional, unintentional, ) | [optional]
**unhealthy_since** | Option<**String**> | When the earliest current stored cause was recorded (the start of the outage); for an intentional disconnect, when it was disconnected. Null when the connection is healthy, including when the account is unhealthy for another reason (analytics, messaging restriction, missing analytics scopes), or when the time is unknown. | [optional]
**analytics_sync** | Option<[**models::GetAllAccountsHealth200ResponseAccountsInnerAnalyticsSync**](GetAllAccountsHealth200ResponseAccountsInnerAnalyticsSync.md)> |  | [optional]
**messaging_restriction** | Option<[**models::GetAccountHealth200ResponseMessagingRestriction**](GetAccountHealth200ResponseMessagingRestriction.md)> |  | [optional]
**platform_connection** | Option<[**models::GetAccountHealth200ResponsePlatformConnection**](GetAccountHealth200ResponsePlatformConnection.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


