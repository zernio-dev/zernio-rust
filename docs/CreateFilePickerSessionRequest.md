# CreateFilePickerSessionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | A Google account connected with `scopes=files`. | 
**redirect_url** | Option<**String**> | Where the browser goes when the user finishes. Absolute `http(s)` URL or a custom app scheme (`myapp://...`); relative, protocol-relative and script URLs are refused. Optional when you rely on the `file.picked` webhook. | [optional]
**file_ids** | Option<**Vec<String>**> | Drive file ids to show the user first (Google Picker `DocsView.setFileIds`), for example to ask for access to files your app already knows about. Pre-navigation only: the user still has to pick them. | [optional]
**mime_types** | Option<**Vec<String>**> | Only show files of these exact media types. | [optional]
**multiselect** | Option<**bool**> | false limits the pick to one file. | [optional][default to true]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


