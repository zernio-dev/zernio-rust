# SelectSnapchatProfileRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** | Your Zernio profile ID | 
**selected_public_profile** | [**models::SelectSnapchatProfileRequestSelectedPublicProfile**](SelectSnapchatProfileRequestSelectedPublicProfile.md) |  | 
**temp_token** | **String** | Temporary Snapchat access token from OAuth | 
**user_profile** | **serde_json::Value** | User profile data from OAuth redirect | 
**refresh_token** | Option<**String**> | Snapchat refresh token (if available) | [optional]
**expires_in** | Option<**i32**> | Token expiration time in seconds | [optional]
**redirect_url** | Option<**String**> | Custom redirect URL after connection completes | [optional]
**oauth_app_id** | Option<**String**> | The `oauthAppId` from the selection redirect, when the connect ran on one of your own OAuth apps. Pass it back so a retried selection stays on that app; a different app than the connect used returns 400. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


