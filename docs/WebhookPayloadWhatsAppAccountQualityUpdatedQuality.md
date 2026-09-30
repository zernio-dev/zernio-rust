# WebhookPayloadWhatsAppAccountQualityUpdatedQuality

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**source** | **Source** | The Meta webhook field that reported the change. (enum: phone_number_quality_update, business_capability_update) | 
**meta_event** | Option<**String**> | Meta's `event` on phone_number_quality_update (for example FLAGGED, UNFLAGGED, UPGRADE, DOWNGRADE, ONBOARDING, THROUGHPUT_UPGRADE). Null on business_capability_update. | 
**quality_rating** | Option<**String**> | Current quality rating (GREEN, YELLOW, RED, UNKNOWN), read live from Meta on FLAGGED/UNFLAGGED. | 
**previous_quality_rating** | Option<**String**> |  | 
**messaging_limit_tier** | Option<**String**> | Current messaging limit tier, for example TIER_250, TIER_2K, TIER_10K, TIER_100K, TIER_UNLIMITED. | 
**previous_messaging_limit_tier** | Option<**String**> |  | 
**display_phone_number** | Option<**String**> |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


