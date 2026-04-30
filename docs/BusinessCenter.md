# BusinessCenter

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bc_id** | Option<**String**> | Business Center ID | [optional]
**name** | Option<**String**> | Display name set by the BC owner | [optional]
**advertiser_count** | Option<**i32**> | Number of advertisers reachable under this BC for the calling token. `null` when the BC asset walk returned empty or failed (typical for agency apps without full BC asset read scope) — distinct from `0`, which would imply the BC genuinely has no advertisers.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


