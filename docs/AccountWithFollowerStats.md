# AccountWithFollowerStats

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: tiktok, instagram, facebook, youtube, linkedin, twitter, threads, pinterest, reddit, bluesky, googlebusiness, telegram, snapchat, discord, whatsapp, linkedinads, metaads, pinterestads, tiktokads, xads, googleads) | [optional]
**profile_id** | Option<[**models::SocialAccountProfileId**](SocialAccountProfileId.md)> |  | [optional]
**username** | Option<**String**> |  | [optional]
**display_name** | Option<**String**> |  | [optional]
**profile_picture** | Option<**String**> | URL to the account's profile picture on the platform. May be null if the platform does not provide one. | [optional]
**profile_url** | Option<**String**> | Full profile URL for the connected account on its platform. | [optional]
**is_active** | Option<**bool**> |  | [optional]
**followers_count** | Option<**f64**> | Follower count (only included if user has analytics add-on) | [optional]
**followers_last_updated** | Option<**String**> | Last time follower count was updated (only included if user has analytics add-on) | [optional]
**parent_account_id** | Option<**String**> | Reference to the parent posting SocialAccount. Set for ads accounts that share or derive from a posting account's OAuth token. null for standalone ads (Google Ads) and all posting accounts.  | [optional]
**enabled** | Option<**bool**> | Whether the user explicitly activated this account. false means the account was created as a side effect (e.g., posting account auto-created when user connected ads first). Posting UI and scheduler ignore accounts with enabled: false.  | [optional]
**metadata** | Option<**serde_json::Value**> | Platform-specific metadata. Fields vary by platform. For WhatsApp accounts, includes: - `qualityRating`: Phone number quality rating from Meta (`GREEN`, `YELLOW`, `RED`, or `UNKNOWN`) - `nameStatus`: Display name review status (`APPROVED`, `PENDING_REVIEW`, `DECLINED`, or `NONE`). Messages cannot be sent until the display name is approved by Meta. - `messagingLimitTier`: Maximum unique business-initiated conversations per 24h rolling window (`TIER_250`, `TIER_1K`, `TIER_10K`, `TIER_100K`, or `TIER_UNLIMITED`). Scales automatically as quality rating improves. - `verifiedName`: Meta-verified business display name - `displayPhoneNumber`: Formatted phone number (e.g., \"+1 555-123-4567\") - `wabaId`: WhatsApp Business Account ID - `phoneNumberId`: Meta phone number ID  | [optional]
**current_followers** | Option<**f64**> | Current follower count | [optional]
**last_updated** | Option<**String**> |  | [optional]
**growth** | Option<**f64**> | Follower change over period | [optional]
**growth_percentage** | Option<**f64**> | Percentage growth | [optional]
**data_points** | Option<**f64**> | Number of historical snapshots | [optional]
**account_stats** | Option<[**models::AccountWithFollowerStatsAllOfAccountStats**](AccountWithFollowerStatsAllOfAccountStats.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


