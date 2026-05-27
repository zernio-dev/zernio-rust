# GetWhatsAppNumberInfo200ResponsePhone

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**display_phone_number** | Option<**String**> |  | [optional]
**verified_name** | Option<**String**> |  | [optional]
**name_status** | Option<**String**> | APPROVED, AVAILABLE_WITHOUT_REVIEW, PENDING_REVIEW, DECLINED, EXPIRED, NONE | [optional]
**quality_rating** | Option<**String**> | GREEN, YELLOW, RED, UNKNOWN | [optional]
**messaging_limit_tier** | Option<**String**> | e.g. TIER_250, TIER_1K, TIER_UNLIMITED | [optional]
**throughput** | Option<[**models::GetWhatsAppNumberInfo200ResponsePhoneThroughput**](GetWhatsAppNumberInfo200ResponsePhoneThroughput.md)> |  | [optional]
**status** | Option<**String**> | e.g. CONNECTED | [optional]
**is_official_business_account** | Option<**bool**> |  | [optional]
**platform_type** | Option<**String**> | e.g. CLOUD_API | [optional]
**health_status** | Option<**serde_json::Value**> | Meta's can_send_message health object (messaging + calling signals) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


