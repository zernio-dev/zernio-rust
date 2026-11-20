# CreateWorkspaceApiKeyRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**permission** | Option<**Permission**> | 'read' restricts the key to GET requests. (enum: read-write, read) | [optional][default to ReadWrite]
**expires_in** | Option<**i32**> | Days until expiry. Omit for a key that never expires. | [optional]
**disabled_resource_groups** | Option<**Vec<DisabledResourceGroups>**> | Resource groups the key cannot use, as on `POST /v1/api-keys`. (enum: publishing, engagement, messages, contacts, analytics, ads, telephony, accounts, billing, webhooks, commerce, creator_campaigns, money, calendar, files) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


