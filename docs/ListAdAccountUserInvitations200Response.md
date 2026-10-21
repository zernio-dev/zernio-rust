# ListAdAccountUserInvitations200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**customer_id** | Option<**String**> |  | [optional]
**invitations** | Option<[**Vec<models::GoogleAdsUserAccessInvitation>**](GoogleAdsUserAccessInvitation.md)> |  | [optional]
**cached_at** | Option<**String**> | When this data was fetched from Google. Null when the cache is unavailable. | [optional]
**stale** | Option<**bool**> | True when Google's quota was exhausted and this is the last successful fetch. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


