# CreateApiKeyRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**expires_in** | Option<**i32**> | Days until expiry | [optional]
**scope** | Option<**Scope**> | 'full' grants access to all profiles (default), 'profiles' restricts to specific profiles (enum: full, profiles) | [optional][default to Full]
**profile_ids** | Option<**Vec<String>**> | Profile IDs this key can access. Required when scope is 'profiles'. | [optional]
**permission** | Option<**Permission**> | 'read-write' allows all operations (default), 'read' restricts to GET requests only (enum: read-write, read) | [optional][default to ReadWrite]
**disabled_resource_groups** | Option<**Vec<DisabledResourceGroups>**> | Resource groups to DISABLE on this key (opt-out denylist). Omit for a legacy full-access key. A key with any group disabled mints with the zrk_ prefix, gets 403 with code=insufficient_permissions and required_group on operations in disabled groups (each operation's group is published as x-resource-group), and can never manage API keys, invites, or member identity. With 'messages' disabled, the KEY cannot access private messages; the ACCOUNT's pre-existing webhook subscriptions are a separate grant surface. (enum: publishing, engagement, messages, contacts, analytics, ads, telephony, accounts, billing, webhooks) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


