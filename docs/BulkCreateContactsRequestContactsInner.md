# BulkCreateContactsRequestContactsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** |  | 
**platform_identifier** | Option<**String**> | Required when the top-level accountId is set (channel mode). A row missing it in that mode is rejected individually and reported in errors[], not a 400 for the whole import. | [optional]
**display_identifier** | Option<**String**> |  | [optional]
**email** | Option<**String**> |  | [optional]
**company** | Option<**String**> |  | [optional]
**tags** | Option<**Vec<String>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


