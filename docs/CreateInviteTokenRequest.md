# CreateInviteTokenRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**scope** | **Scope** | 'all' grants access to all profiles, 'profiles' restricts to specific profiles (enum: all, profiles) | 
**profile_ids** | Option<**Vec<String>**> | Required if scope is 'profiles'. Array of profile IDs to grant access to. | [optional]
**role** | Option<**Role**> | Org role granted to the invitee. Defaults to 'member'. 'admin' can manage the team (invite/remove members, change roles and access) and billing, but not ownership transfer or account deletion. 'billing_admin' (displayed as Billing Manager) manages billing only. 'viewer' creates a read-only member who can view everything in their profile scope but cannot perform any content mutation (publish, edit, delete, connect accounts). (enum: admin, member, billing_admin, viewer) | [optional][default to Member]
**read_only** | Option<**bool**> | Deprecated. Use role 'viewer' instead. When true, the invite is created with role 'viewer'. Cannot be combined with role 'billing_admin' or 'admin'. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


