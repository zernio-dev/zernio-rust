# ListContactGroups200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Google contactGroups/{id}; Outlook folder:{folderId} (folder:default for the default Contacts folder) or category:{name}. | [optional]
**name** | Option<**String**> |  | [optional]
**r#type** | Option<**Type**> |  (enum: group, folder, category) | [optional]
**system** | Option<**bool**> | A group the provider defines, such as Google starred or the default Outlook Contacts folder. | [optional]
**member_count** | Option<**i32**> | Members as Google counts them. Null for Outlook. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


