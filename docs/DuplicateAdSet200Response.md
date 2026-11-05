# DuplicateAdSet200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**copied_ad_set_id** | Option<**String**> | Platform ID of the new ad set | [optional]
**copied_ad_ids** | Option<**Vec<String>**> | Platform IDs of the copied ads | [optional]
**ad_id_map** | Option<**std::collections::HashMap<String, String>**> | Meta only: source ad ID to copied ad ID. Empty when `deepCopy` is false. | [optional]
**discovery** | Option<**Discovery**> | The copy exists on the platform in all three cases.  - `triggered`: an ads sync started and runs after this response, so the copy may not be readable through Zernio yet. - `skipped`: no sync started, so the copy appears on a later scheduled sync. - `failed`: the sync could not start. A sync that errors after the response is not reported here. (enum: triggered, skipped, failed) | [optional]
**raw** | Option<**serde_json::Value**> | Platform-native response from the copy (TikTok). Absent on Meta, which returns `adIdMap` instead. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


