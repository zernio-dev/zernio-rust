# GetCurrentUser200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**email** | Option<**String**> | Only returned to a dashboard session. Omitted for API keys. | [optional]
**image** | Option<**String**> |  | [optional]
**role** | Option<**String**> | One of owner, admin, billing_admin, member or viewer. Always owner when isRoot is true. | [optional]
**is_root** | Option<**bool**> | True when the user owns the account, false when they were invited to it. | [optional]
**invited_by** | Option<**String**> | Id of the user who invited this user. Null when isRoot is true. | [optional]
**invited_to_profile** | Option<**String**> | Only present when isRoot is false. | [optional]
**invited_to_profiles** | Option<**Vec<String>**> | Ids of the profiles an invited user is limited to. Empty means every profile. Only present when isRoot is false. | [optional]
**disabled_resource_groups** | Option<**Vec<String>**> | Resource groups turned off for an invited user. Null or empty means none. Only present when isRoot is false. | [optional]
**created_at** | Option<**String**> |  | [optional]
**last_login_at** | Option<**String**> | Last sign-in, stamped at most once an hour. Null when no sign-in has been recorded. | [optional]
**workspace_id** | Option<**String**> | Id of the workspace the credential acts in. Null when the user has no workspace yet. | [optional]
**workspace_name** | Option<**String**> | Name of that workspace. Null when workspaceId is null. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


