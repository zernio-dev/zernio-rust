# ListFacebookPages200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pages** | Option<[**Vec<models::ListFacebookPages200ResponsePagesInner>**](ListFacebookPages200ResponsePagesInner.md)> |  | [optional]
**truncated** | Option<**bool**> | True when Meta still had more Pages after the listing hit its time budget or the 10,000 Page cap, so `pages` is incomplete. Do not ask the user to reconnect with fewer Pages ticked: Meta replaces the Page grant on every authorization, so unticked Pages lose access. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


