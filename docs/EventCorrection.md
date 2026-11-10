# EventCorrection

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> |  | [optional]
**destination_id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**status** | Option<**Status**> | `corrected`: the platform changed its count. `not_supported`: the platform has no API to change a conversion it already counted. `failed`: see `error`. (enum: corrected, not_supported, failed) | [optional]
**error** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


