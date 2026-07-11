# UpdateAdStatus200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**updated** | Option<**i32**> | 1 when the status changed, 0 when skipped | [optional]
**skipped** | Option<**i32**> | 1 when skipped (terminal status or already in target state), else 0 | [optional]
**message** | Option<**String**> | Human-readable summary (present only when skipped) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


