# BulkUploadResult

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | Option<**i32**> | Number of data rows processed from the CSV | [optional]
**valid** | Option<**i32**> | Count of rows that succeeded (results[].ok === true) | [optional]
**invalid** | Option<**i32**> | Count of rows that failed (total - valid) | [optional]
**results** | Option<[**Vec<models::BulkUploadResultResultsInner>**](BulkUploadResultResultsInner.md)> | One entry per CSV data row, in row order. | [optional]
**warnings** | Option<**Vec<String>**> | Top-level advisory warnings (e.g. `rows_exceed_advisory_limit:500`). Empty when none. | [optional]
**rate_limited_accounts** | Option<[**Vec<models::BulkUploadResultRateLimitedAccountsInner>**](BulkUploadResultRateLimitedAccountsInner.md)> | Present only when one or more rows targeted an account currently in cooldown. Lets callers map `rate_limited:*` row errors back to structured metadata without parsing the error strings.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


