# InboxWebhookAccount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Account ID | 
**account_id** | Option<**String**> | Account ID (same value as id). Canonical field so consumers can filter every webhook event on one field (e.g. route staging vs production by account). id is kept for backward compatibility. | [optional]
**profile_id** | Option<**String**> | Zernio profile ID this account belongs to. Use it to route or filter inbox webhooks by profile.  This is the profile ID only, not its name (resolve the name via the API with this ID). Optional: omitted on the shared WhatsApp sandbox account and when the account has no resolvable profile.  | [optional]
**platform** | **String** |  | 
**username** | **String** |  | 
**display_name** | Option<**String**> |  | [optional]
**page_id** | Option<**String**> | The bare Facebook Page id behind the account, to route inbound messages by Page. Present for Facebook accounts and Instagram accounts connected through Facebook Login; omitted otherwise. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


