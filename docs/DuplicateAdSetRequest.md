# DuplicateAdSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **Platform** |  (enum: facebook, instagram, tiktok) | 
**campaign_id** | Option<**String**> | Destination platform campaign id (defaults to the source's campaign) | [optional]
**deep_copy** | Option<**bool**> | Copy child ads + creatives | [optional][default to true]
**status_option** | Option<**StatusOption**> |  (enum: ACTIVE, PAUSED, INHERITED_FROM_SOURCE) | [optional][default to Paused]
**start_time** | Option<**String**> | Reschedule the copy's start (ISO 8601). A value without an offset (`YYYY-MM-DD`, `YYYY-MM-DD HH:MM:SS` or `YYYY-MM-DDTHH:MM:SS`) is read in the ad account timezone. | [optional]
**end_time** | Option<**String**> | Reschedule the copy's end, read like `startTime`; a date-only end runs to 23:59:59 local. | [optional]
**rename_strategy** | Option<**RenameStrategy**> | Meta's native `rename_strategy` values. `DEEP_RENAME` renames the copied ad set and its copied ads with `renamePrefix` / `renameSuffix`. `ONLY_TOP_LEVEL_RENAME` renames only the copied ad set; its ads keep their source names. `NO_RENAME` keeps every source name. With no rename option at all, Meta appends its own ` - Copy` suffix. Ignored on TikTok, where `renamePrefix` / `renameSuffix` still apply. (enum: DEEP_RENAME, ONLY_TOP_LEVEL_RENAME, NO_RENAME) | [optional]
**rename_prefix** | Option<**String**> | Text prepended to each renamed object's name. | [optional]
**rename_suffix** | Option<**String**> | Text appended to each renamed object's name. | [optional]
**sync_after** | Option<**bool**> |  | [optional][default to true]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


