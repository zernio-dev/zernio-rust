# PostsListResponsePagination

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**page** | Option<**i32**> |  | [optional]
**limit** | Option<**i32**> |  | [optional]
**total** | Option<**i32**> |  | [optional]
**pages** | Option<**i32**> |  | [optional]
**next_cursor** | Option<**String**> | Cursor for the next page in the same sortBy order. Send it back as `cursor`. Null on the last page, and always null for `sortBy=status` or `sortBy=platform`. Absent for `source=external`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


