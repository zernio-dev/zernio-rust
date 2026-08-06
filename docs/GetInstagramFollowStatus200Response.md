# GetInstagramFollowStatus200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user_id** | **String** |  | 
**account_id** | **String** |  | 
**is_follower** | Option<**bool**> | The user follows this account. Null = unknown, never \"no\". | 
**is_followed_by_account** | Option<**bool**> | This account follows the user. | [optional]
**follower_count** | Option<**i32**> |  | [optional]
**is_verified** | Option<**bool**> |  | [optional]
**username** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**unavailable_reason** | Option<**UnavailableReason**> | Why the follow relationship could not be resolved. Null when it was. (enum: consent_required, dm_access_disabled, not_messageable, error, ) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


