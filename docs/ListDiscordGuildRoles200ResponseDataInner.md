# ListDiscordGuildRoles200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Role snowflake ID | [optional]
**name** | Option<**String**> |  | [optional]
**color** | Option<**i32**> | Decimal color (0 = no color). Convert to hex via .toString(16). | [optional]
**position** | Option<**i32**> | Position in role hierarchy (higher = more authority) | [optional]
**permissions** | Option<**String**> | Permissions bitfield as a stringified integer | [optional]
**managed** | Option<**bool**> | True for integration-managed roles (bot roles) | [optional]
**mentionable** | Option<**bool**> |  | [optional]
**hoist** | Option<**bool**> | True if role is displayed separately in member list | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


