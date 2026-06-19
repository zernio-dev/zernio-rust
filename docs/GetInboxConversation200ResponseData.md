# GetInboxConversation200ResponseData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**account_username** | Option<**String**> |  | [optional]
**platform** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: active, archived) | [optional]
**participant_name** | Option<**String**> |  | [optional]
**participant_id** | Option<**String**> |  | [optional]
**participant_verified_type** | Option<**ParticipantVerifiedType**> | X/Twitter verified badge type. Only present for Twitter/X conversations. (enum: blue, government, business, none) | [optional]
**last_message** | Option<**String**> |  | [optional]
**last_message_at** | Option<**String**> |  | [optional]
**updated_time** | Option<**String**> |  | [optional]
**participants** | Option<[**Vec<models::UpdateFacebookPage200ResponseSelectedPage>**](UpdateFacebookPage200ResponseSelectedPage.md)> |  | [optional]
**instagram_profile** | Option<[**models::ListInboxConversations200ResponseDataInnerInstagramProfile**](ListInboxConversations200ResponseDataInnerInstagramProfile.md)> |  | [optional]
**metadata** | Option<**std::collections::HashMap<String, String>**> | Ad-click attribution captured on the first inbound message of the conversation. Only present when the conversation originated from a click-to-message ad. Absent on organic conversations.  Two sources populate this field:   - WhatsApp CTWA (Click-to-WhatsApp): `ctwa_clid`, `ctwa_source_id`,     `ctwa_source_url`, `ctwa_headline`, `ctwa_source_type`, `ctwa_captured_at`.   - Facebook Messenger CTM / Instagram CTD: `meta_ad_id`, `meta_ad_title`,     `meta_ad_source`, `meta_ad_type`, `meta_ad_ref`, `meta_ad_captured_at`,     `meta_ad_photo_url`, `meta_ad_video_url`, `meta_ad_post_id`,     `meta_ad_product_id`, `meta_ad_flow_id`.  Note: `meta_ad_photo_url` and `meta_ad_video_url` are Facebook CDN URLs that may expire. Use `meta_ad_id` for a permanent reference to the ad (e.g. to link to Meta Ads Manager).  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


