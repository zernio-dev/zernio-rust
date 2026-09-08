# AdKeyword

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> | Account ID owning the sync | [optional]
**profile_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: google) | [optional]
**ad_account_id** | Option<**String**> | Google customer ID | [optional]
**campaign_id** | Option<**String**> |  | [optional]
**campaign_name** | Option<**String**> |  | [optional]
**campaign_status** | Option<**String**> |  | [optional]
**ad_set_id** | Option<**String**> | Google ad group ID | [optional]
**ad_set_name** | Option<**String**> |  | [optional]
**ad_set_status** | Option<**String**> |  | [optional]
**keyword** | Option<**String**> |  | [optional]
**match_type** | Option<**MatchType**> |  (enum: exact, phrase, broad, unknown) | [optional]
**status** | Option<**Status**> |  (enum: active, paused) | [optional]
**negative** | Option<**bool**> |  | [optional]
**quality_score** | Option<**i32**> | Google Quality Score, 1-10. Null when unrated. | [optional]
**synced_at** | Option<**String**> |  | [optional]
**metrics** | Option<[**models::AdKeywordMetrics**](AdKeywordMetrics.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


