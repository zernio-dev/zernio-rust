# DuplicateAdSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **Platform** |  (enum: facebook, instagram) | 
**campaign_id** | Option<**String**> | Destination platform campaign id (defaults to the source's campaign) | [optional]
**deep_copy** | Option<**bool**> | Copy child ads + creatives | [optional][default to true]
**status_option** | Option<**StatusOption**> |  (enum: ACTIVE, PAUSED, INHERITED_FROM_SOURCE) | [optional][default to Paused]
**start_time** | Option<**String**> | Reschedule the copy's start time | [optional]
**end_time** | Option<**String**> |  | [optional]
**rename_strategy** | Option<**RenameStrategy**> |  (enum: DEEP_RENAME, ONLY_TOP_LEVEL_RENAME, NO_RENAME) | [optional]
**rename_prefix** | Option<**String**> |  | [optional]
**rename_suffix** | Option<**String**> |  | [optional]
**sync_after** | Option<**bool**> |  | [optional][default to true]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


