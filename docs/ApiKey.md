# ApiKey

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**key_preview** | Option<**String**> |  | [optional]
**expires_at** | Option<**String**> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**key** | Option<**String**> | Returned only once, on creation | [optional]
**scope** | Option<**Scope**> | 'full' grants access to all profiles, 'profiles' restricts to specific profiles (enum: full, profiles) | [optional][default to Full]
**profile_ids** | Option<[**Vec<models::ApiKeyProfileIdsInner>**](ApiKeyProfileIdsInner.md)> | Profiles this key can access (populated with name and color). Only present when scope is 'profiles'. | [optional]
**permission** | Option<**Permission**> | 'read-write' allows all operations, 'read' restricts to GET requests only (enum: read-write, read) | [optional][default to ReadWrite]
**disabled_resource_groups** | Option<**Vec<DisabledResourceGroups>**> | Resource groups this key can NOT access (opt-out denylist). Absent or empty means legacy full access. A key with any group disabled is a restricted key (zrk_ prefix) and can never manage API keys, invites, or member identity. Each operation's group is published as x-resource-group. With 'messages' disabled, the key cannot read or send private messages through any API surface, and it cannot create or edit a webhook subscription broader than itself: it cannot subscribe to, test-fire, redeliver, or read delivery logs for message events. Subscriptions created earlier, from the dashboard, or with a full-access key keep delivering whatever their own `disabledResourceGroups` allows, so restricting an existing integration end to end means restricting the subscription too. OAuth connector tokens (AI assistants and MCP clients) resolve against the same registry, but their groups are not settable yet: treat an authorized connector as full access. (enum: publishing, engagement, messages, contacts, analytics, ads, telephony, accounts, billing, webhooks) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


