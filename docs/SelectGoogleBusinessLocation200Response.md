# SelectGoogleBusinessLocation200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | Option<**String**> |  | [optional]
**redirect_url** | Option<**String**> | Redirect URL if custom redirect_url was provided | [optional]
**account** | Option<[**models::SelectGoogleBusinessLocation200ResponseAccount**](SelectGoogleBusinessLocation200ResponseAccount.md)> |  | [optional]
**accounts** | Option<**Vec<serde_json::Value>**> | locations with two or more distinct entries only. The connected accounts, same shape as `account`. The redirect_url then carries `accountIds` (comma-separated) and `accountId` of the first. | [optional]
**failed** | Option<[**Vec<models::SelectGoogleBusinessLocation200ResponseFailedInner>**](SelectGoogleBusinessLocation200ResponseFailedInner.md)> | locations only. The locations that could not be connected while the others were. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


