# ConnectLineCredentialsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel_id** | **String** | The Messaging API channel's Channel ID (digits only). | 
**channel_secret** | **String** | The Messaging API channel's Channel secret (32 hex characters). | 
**state** | **String** | Required state formatted as {userId}-{profileId}. Get userId from GET /v1/users and profileId from GET /v1/profiles. | 
**redirect_url** | Option<**String**> | Optional URL to redirect to after a successful connection. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


