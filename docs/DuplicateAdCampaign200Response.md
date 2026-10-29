# DuplicateAdCampaign200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**copied_campaign_id** | Option<**String**> | Platform ID of the new campaign | [optional]
**ad_set_id_map** | Option<**std::collections::HashMap<String, String>**> | Meta only: source ad set ID to copied ad set ID. Empty when `deepCopy` is false. | [optional]
**ad_id_map** | Option<**std::collections::HashMap<String, String>**> | Meta only: source ad ID to copied ad ID, across every copied ad set. Empty when `deepCopy` is false. | [optional]
**discovery** | Option<**Discovery**> |  (enum: triggered, skipped, failed) | [optional]
**raw** | Option<**serde_json::Value**> | Platform-native response from the copy (TikTok and LinkedIn). Absent on Meta, which returns `adSetIdMap` and `adIdMap` instead. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


