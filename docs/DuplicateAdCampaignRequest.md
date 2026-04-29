# DuplicateAdCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **Platform** |  (enum: facebook, instagram, tiktok) | 
**deep_copy** | Option<**bool**> | Copy child ad sets + ads + creatives + targeting | [optional][default to true]
**status_option** | Option<**StatusOption**> |  (enum: ACTIVE, PAUSED, INHERITED_FROM_SOURCE) | [optional][default to Paused]
**start_time** | Option<**String**> | Reschedule the copied hierarchy's start time | [optional]
**end_time** | Option<**String**> |  | [optional]
**rename_strategy** | Option<**RenameStrategy**> |  (enum: DEEP_RENAME, ONLY_TOP_LEVEL_RENAME, NO_RENAME) | [optional]
**rename_prefix** | Option<**String**> |  | [optional]
**rename_suffix** | Option<**String**> |  | [optional]
**sync_after** | Option<**bool**> | Trigger ads discovery on the owning account after the copy succeeds | [optional][default to true]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


