# SocialAccount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: tiktok, instagram, facebook, youtube, linkedin, twitter, threads, pinterest, reddit, bluesky, googlebusiness, telegram, snapchat, whatsapp, linkedinads, metaads, pinterestads, tiktokads, xads, googleads) | [optional]
**profile_id** | Option<[**models::SocialAccountProfileId**](SocialAccountProfileId.md)> |  | [optional]
**username** | Option<**String**> |  | [optional]
**display_name** | Option<**String**> |  | [optional]
**profile_url** | Option<**String**> | Full profile URL for the connected account on its platform. | [optional]
**is_active** | Option<**bool**> |  | [optional]
**followers_count** | Option<**f64**> | Follower count (only included if user has analytics add-on) | [optional]
**followers_last_updated** | Option<**String**> | Last time follower count was updated (only included if user has analytics add-on) | [optional]
**parent_account_id** | Option<**String**> | Reference to the parent posting SocialAccount. Set for ads accounts that share or derive from a posting account's OAuth token. null for standalone ads (Google Ads) and all posting accounts.  | [optional]
**enabled** | Option<**bool**> | Whether the user explicitly activated this account. false means the account was created as a side effect (e.g., posting account auto-created when user connected ads first). Posting UI and scheduler ignore accounts with enabled: false.  | [optional]
**ads_status** | Option<**AdsStatus**> | **Deprecated.** With the new ads account model, ads accounts are separate SocialAccount documents. Check for accounts with ads platform values (metaads, linkedinads, pinterestads, tiktokads, xads, googleads) instead.  Legacy behavior: - `connected`: Ads are ready to use (same-token platforms like Meta/LinkedIn, or separate ads token is present). - `not_connected`: Platform supports ads but requires a separate ads OAuth. Use `GET /v1/connect/{platform}/ads` to connect. - `not_available`: Platform does not support ads (e.g., YouTube, Reddit, Bluesky).  (enum: connected, not_connected, not_available) | [optional]
**metadata** | Option<**serde_json::Value**> | Platform-specific metadata. Fields vary by platform. For WhatsApp accounts, includes: - `qualityRating`: Phone number quality rating from Meta (`GREEN`, `YELLOW`, `RED`, or `UNKNOWN`) - `nameStatus`: Display name review status (`APPROVED`, `PENDING_REVIEW`, `DECLINED`, or `NONE`). Messages cannot be sent until the display name is approved by Meta. - `messagingLimitTier`: Maximum unique business-initiated conversations per 24h rolling window (`TIER_250`, `TIER_1K`, `TIER_10K`, `TIER_100K`, or `TIER_UNLIMITED`). Scales automatically as quality rating improves. - `verifiedName`: Meta-verified business display name - `displayPhoneNumber`: Formatted phone number (e.g., \"+1 555-123-4567\") - `wabaId`: WhatsApp Business Account ID - `phoneNumberId`: Meta phone number ID  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


