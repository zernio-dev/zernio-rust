# SelectInstagramAccountRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** | Profile ID from your connection flow | 
**page_id** | Option<**String**> | The Facebook Page ID selected by the user, from GET /v1/connect/instagram/select-account. Send this or pageIds, not both. | [optional]
**page_ids** | Option<**Vec<String>**> | Several Page IDs whose linked Instagram accounts to connect from one sign-in, each as its own account. With two or more distinct IDs the response lists `accounts` and `failed` instead of `account`, and the request is refused with 400 on a reconnect or an ads connect. A single distinct ID behaves exactly like pageId. | [optional]
**temp_token** | **String** | Long-lived Facebook user access token from the OAuth callback redirect | 
**redirect_url** | Option<**String**> | Optional custom redirect URL to return to after selection | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


