# ConnectOpenAiAdsCredentialsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**api_key** | **String** | API key from ChatGPT Ads Manager (Settings). Grants full read/write access on OpenAI's side; Zernio only ever reads with it. | 
**profile_id** | **String** | Your Zernio profile ID | 
**state** | Option<**String**> | Optional state passthrough for the connect flow. | [optional]
**redirect_url** | Option<**String**> | Optional URL to redirect to after successful connection, echoed back as redirectUrl. | [optional]
**redirect_uri** | Option<**String**> | Alias of redirect_url, kept for existing callers | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


