# GetAccountHealth200ResponsePermissions

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**posting** | Option<[**Vec<models::GetAccountHealth200ResponsePermissionsPostingInner>**](GetAccountHealth200ResponsePermissionsPostingInner.md)> |  | [optional]
**analytics** | Option<[**Vec<models::GetAccountHealth200ResponsePermissionsPostingInner>**](GetAccountHealth200ResponsePermissionsPostingInner.md)> |  | [optional]
**optional** | Option<[**Vec<models::GetAccountHealth200ResponsePermissionsPostingInner>**](GetAccountHealth200ResponsePermissionsPostingInner.md)> |  | [optional]
**can_post** | Option<**bool**> | Whether the granted OAuth scopes allow posting. Scopes only: for WhatsApp, whether Meta lets the number send is `platformConnection.phoneStatus` and the overall `status`. | [optional]
**can_fetch_analytics** | Option<**bool**> |  | [optional]
**analytics_supported** | Option<**bool**> | Whether analytics is in scope for this account at all (the platform offers analytics and it was requested at connect). False means canFetchAnalytics is not a problem to fix; true with canFetchAnalytics false means analytics needs a reconnect. | [optional]
**missing_required** | Option<**Vec<String>**> |  | [optional]
**scope_areas** | Option<**std::collections::HashMap<String, Inner>**> | Present when the account connected with `scopes` or through your own OAuth app: each permission area the platform splits, as granted, missing or not_requested. An area never requested does not make the account unhealthy. (enum: granted, missing, not_requested) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


