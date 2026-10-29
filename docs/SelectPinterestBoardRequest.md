# SelectPinterestBoardRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** | Your Zernio profile ID | 
**board_id** | **String** | The Pinterest Board ID selected by the user | 
**board_name** | Option<**String**> | The board name (for display purposes) | [optional]
**temp_token** | **String** | Temporary Pinterest access token from OAuth | 
**user_profile** | Option<**serde_json::Value**> | User profile data from OAuth redirect | [optional]
**refresh_token** | Option<**String**> | Pinterest refresh token (if available) | [optional]
**expires_in** | Option<**i32**> | Token expiration time in seconds | [optional]
**redirect_url** | Option<**String**> | Custom redirect URL after connection completes | [optional]
**oauth_app_id** | Option<**String**> | The `oauthAppId` from the selection redirect, when the connect ran on one of your own OAuth apps. Pass it back so a retried selection stays on that app; a different app than the connect used returns 400. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


