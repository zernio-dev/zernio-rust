# ConnectWechatCredentialsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**app_id** | **String** | The Official Account's AppID (starts with wx). | 
**app_secret** | **String** | The Official Account's AppSecret (32 characters). | 
**state** | **String** | Required state formatted as {userId}-{profileId}. Get userId from GET /v1/users and profileId from GET /v1/profiles. | 
**display_name** | Option<**String**> | Name to show for the account. Defaults to \"WeChat Official Account\". | [optional]
**redirect_url** | Option<**String**> | Optional URL to redirect to after a successful connection. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


