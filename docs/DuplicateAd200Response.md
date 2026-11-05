# DuplicateAd200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**copied_ad_id** | Option<**String**> | Platform ID of the new ad | [optional]
**discovery** | Option<**Discovery**> | The copy exists on the platform in all three cases.  - `triggered`: an ads sync started and runs after this response, so the copy may not be readable through Zernio yet. - `skipped`: no sync started, so the copy appears on a later scheduled sync. - `failed`: the sync could not start. A sync that errors after the response is not reported here. (enum: triggered, skipped, failed) | [optional]
**raw** | Option<**serde_json::Value**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


