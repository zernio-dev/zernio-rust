# SocialAccount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**profile_id** | Option<[**models::SocialAccountProfileId**](SocialAccountProfileId.md)> |  | [optional]
**username** | Option<**String**> |  | [optional]
**display_name** | Option<**String**> |  | [optional]
**profile_url** | Option<**String**> | Full profile URL for the connected account on its platform. | [optional]
**is_active** | Option<**bool**> |  | [optional]
**followers_count** | Option<**f64**> | Follower count (only included if user has analytics add-on) | [optional]
**followers_last_updated** | Option<**String**> | Last time follower count was updated (only included if user has analytics add-on) | [optional]
**metadata** | Option<**serde_json::Value**> | Platform-specific metadata. Fields vary by platform. For WhatsApp accounts, includes: - `qualityRating`: Phone number quality rating from Meta (`GREEN`, `YELLOW`, `RED`, or `UNKNOWN`) - `nameStatus`: Display name review status (`APPROVED`, `PENDING_REVIEW`, `DECLINED`, or `NONE`). Messages cannot be sent until the display name is approved by Meta. - `messagingLimitTier`: Maximum unique business-initiated conversations per 24h rolling window (`TIER_250`, `TIER_1K`, `TIER_10K`, `TIER_100K`, or `TIER_UNLIMITED`). Scales automatically as quality rating improves. - `verifiedName`: Meta-verified business display name - `displayPhoneNumber`: Formatted phone number (e.g., \"+1 555-123-4567\") - `wabaId`: WhatsApp Business Account ID - `phoneNumberId`: Meta phone number ID  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


