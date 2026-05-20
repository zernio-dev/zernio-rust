# BulkUploadResultResultsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**row_index** | Option<**i32**> | 1-based index of the CSV data row (header excluded) | [optional]
**ok** | Option<**bool**> | Whether the row was created successfully | [optional]
**created_post_id** | Option<**String**> | ID of the created post. Present only when `ok` is true and not a dry run. | [optional]
**errors** | Option<**Vec<String>**> | Machine-readable failure codes for this row. Present only when `ok` is false. Examples: `unknown_profile:<id>`, `no_account_for_platform:<platform>`, `schedule_time_missing`, `rate_limited:<platform>:@<username>:<remaining>`.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


