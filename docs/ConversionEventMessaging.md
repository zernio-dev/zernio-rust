# ConversionEventMessaging

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel** | **Channel** |  (enum: whatsapp, messenger, instagram_direct) | 
**waba_id** | Option<**String**> | WhatsApp only. WhatsApp Business Account id, sent as `whatsapp_business_account_id`. | [optional]
**ctwa_clid** | Option<**String**> | WhatsApp only. Click-to-WhatsApp click id from the first inbound message referral, sent as `ctwa_clid`. | [optional]
**page_id** | Option<**String**> | Messenger: Facebook Page id, sent as `page_id`. Instagram Direct: when `instagramBusinessAccountId` is absent, Zernio reads the Instagram professional account linked to this Page and sends its id as `ig_account_id`; if none is linked or the lookup fails, `page_id` is sent instead. | [optional]
**instagram_business_account_id** | Option<**String**> | Instagram Direct only. Instagram professional account id (`instagram_business_account` on the Page), sent as `ig_account_id` next to `ig_sid`. | [optional]
**page_scoped_user_id** | Option<**String**> | Messenger only. The page-scoped user id (PSID) your Messenger webhook gives for the person, sent as `page_scoped_user_id` next to `page_id`. | [optional]
**instagram_scoped_user_id** | Option<**String**> | Instagram Direct only. The Instagram-scoped user id (IGSID) your Instagram messaging webhook gives for the person, sent as `ig_sid`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


