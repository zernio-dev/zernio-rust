# CreatePlatformInviteRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** | The profile the account is connected to. | 
**platform** | **Platform** |  (enum: facebook, instagram, linkedin, twitter, threads, tiktok, youtube, pinterest, reddit, bluesky, snapchat, googlebusiness) | 
**account_id** | Option<**String**> | Reconnect this existing account instead of adding a new one. It must belong to the profile and platform. | [optional]
**login_method** | Option<**LoginMethod**> | Instagram only. instagram_login (the default) uses Instagram Login, facebook_login uses Facebook Login. A reconnect link keeps the method the account was connected with. (enum: instagram_login, facebook_login) | [optional]
**expires_in_days** | Option<**i32**> | Days until the link expires. | [optional][default to 7]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


