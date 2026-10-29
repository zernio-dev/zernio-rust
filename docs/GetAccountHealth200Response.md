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
**analytics_sync** | Option<[**models::GetAllAccountsHealth200ResponseAccountsInnerAnalyticsSync**](GetAllAccountsHealth200ResponseAccountsInnerAnalyticsSync.md)> |  | [optional]
**messaging_restriction** | Option<[**models::GetAccountHealth200ResponseMessagingRestriction**](GetAccountHealth200ResponseMessagingRestriction.md)> |  | [optional]
**platform_connection** | Option<[**models::GetAccountHealth200ResponsePlatformConnection**](GetAccountHealth200ResponsePlatformConnection.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


