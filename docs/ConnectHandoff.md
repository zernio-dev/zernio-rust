# ConnectHandoff

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**uuid::Uuid**> |  | [optional]
**status** | Option<**Status**> |  (enum: waiting, opened, connected, failed, expired) | [optional]
**platform** | Option<**String**> |  | [optional]
**accounts** | Option<[**Vec<models::ConnectHandoffAccountsInner>**](ConnectHandoffAccountsInner.md)> | Filled when `status` is `connected`: every account the connect added (several when the user picked several pages, locations or organizations), each checked to be on the profile the connect was started for and written during this handoff. Empty otherwise. | [optional]
**error** | Option<[**models::ConnectHandoffError**](ConnectHandoffError.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


