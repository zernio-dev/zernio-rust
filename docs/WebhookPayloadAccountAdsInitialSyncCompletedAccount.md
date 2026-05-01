# WebhookPayloadAccountAdsInitialSyncCompletedAccount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | The account's unique identifier (same as used in /v1/accounts/{accountId}) | 
**profile_id** | **String** | The profile's unique identifier this account belongs to | 
**platform** | **String** |  | 
**username** | **String** |  | 
**display_name** | Option<**String**> |  | [optional]
**platform_user_id** | Option<**String**> | The platform-side account/ad-account ID (e.g. Meta ad account ID). | [optional]
**profile_picture** | Option<**String**> | URL of the account's profile picture, when available. | [optional]
**platform_ad_account_id** | Option<**String**> | When the consumer scoped the connect call to a single ad account, this echoes that ID back so the webhook can be correlated to the originating connect request without consulting the consumer's DB. Meta uses the `act_*` shape.  | [optional]
**platform_ad_account_ids** | Option<**Vec<String>**> | Every ad-account ID that the connected token could see at discovery time. Useful for \"we synced ads from these accounts\" UX without a follow-up API call. Empty array when the token had no ad-account visibility.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


