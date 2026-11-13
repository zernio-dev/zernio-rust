# ListEmailFolders200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | Option<[**Vec<models::EmailFolder>**](EmailFolder.md)> |  | [optional]
**stale** | Option<**bool**> | Always true when present. Present only when the provider did not answer and `data` is the last folder list Zernio read for the same account within the past 24 hours (`unreadCount` and `totalCount` may be out of date). | [optional]
**as_of** | Option<**String**> | When a stale list was read from the provider. Present only with `stale`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


