# DuplicateAdCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **Platform** |  (enum: facebook, instagram, tiktok, linkedin) | 
**deep_copy** | Option<**bool**> | Copy child ad sets + ads + creatives + targeting | [optional][default to true]
**status_option** | Option<**StatusOption**> | ACTIVE = launch the clone immediately (spends the moment LinkedIn approves it). PAUSED = clone stays DRAFT, safe default. INHERITED_FROM_SOURCE = mirror each entity's source status per-entity. Duplicating an ACTIVE campaign this way starts a second front of spend.  (enum: ACTIVE, PAUSED, INHERITED_FROM_SOURCE) | [optional][default to Paused]
**start_time** | Option<**String**> | Reschedule the copied hierarchy's start (ISO 8601). On Meta and TikTok a value without an offset (`YYYY-MM-DD`, `YYYY-MM-DD HH:MM:SS` or `YYYY-MM-DDTHH:MM:SS`) is read in the ad account timezone; LinkedIn ad accounts carry no timezone, so there it is read as UTC. TikTok defaults to a start a few minutes after the copy. | [optional]
**end_time** | Option<**String**> | Reschedule the copied hierarchy's end, read like `startTime`; a date-only end runs to 23:59:59 local. Defaults to the source's end. | [optional]
**rename_strategy** | Option<**RenameStrategy**> |  (enum: DEEP_RENAME, ONLY_TOP_LEVEL_RENAME, NO_RENAME) | [optional]
**rename_prefix** | Option<**String**> |  | [optional]
**rename_suffix** | Option<**String**> |  | [optional]
**sync_after** | Option<**bool**> | Trigger ads discovery on the owning account after the copy succeeds | [optional][default to true]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


