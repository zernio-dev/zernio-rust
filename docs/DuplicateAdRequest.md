# DuplicateAdRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_set_id** | Option<**String**> | Destination platform ad set id (defaults to the source's ad set) | [optional]
**status_option** | Option<**StatusOption**> |  (enum: ACTIVE, PAUSED, INHERITED_FROM_SOURCE) | [optional][default to Paused]
**rename_strategy** | Option<**RenameStrategy**> |  (enum: DEEP_RENAME, ONLY_TOP_LEVEL_RENAME, NO_RENAME) | [optional]
**rename_prefix** | Option<**String**> |  | [optional]
**rename_suffix** | Option<**String**> |  | [optional]
**sync_after** | Option<**bool**> |  | [optional][default to true]
**reuse_source_creative** | Option<**bool**> | Point the copy at the source ad's creative object instead of copying it, so the copy keeps the same Facebook post, the same Instagram media, their existing likes, comments and shares, and the full creative setup (text variations included). This is what Ads Manager's \"show existing reactions, comments and shares\" does. Meta's native copy always publishes new posts. A creative belongs to one ad account, so `adSetId` must be in the source ad's account. 400 when the source ad has no creative yet. | [optional][default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


