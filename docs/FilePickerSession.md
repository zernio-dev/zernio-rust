# FilePickerSession

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Public session id, echoed as `pickerSessionId` on the redirect and as `picker.sessionId` on the webhook. | 
**url** | **String** | The hosted picker page. Open it in the end user's browser (redirect or new tab, not an iframe). It is a credential: single-use and valid until `expiresAt`. | 
**expires_at** | **String** | 30 minutes after creation. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


