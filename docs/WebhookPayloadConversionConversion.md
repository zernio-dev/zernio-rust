# WebhookPayloadConversionConversion

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event_id** | **String** |  | 
**event_name** | **String** |  | 
**event_time** | **String** |  | 
**received_at** | **String** |  | 
**source** | **String** | Who sent it: `api`, `relay`, a lead form (`meta_leads`, `google_leads`, `linkedin_leads`, `tiktok_leads`), a store (`shopify`, `woocommerce`) or `hubspot`. | 
**action_source** | Option<**String**> |  | [optional]
**value** | Option<**f64**> |  | [optional]
**currency** | Option<**String**> |  | [optional]
**source_url** | Option<**String**> | Origin, path and attribution parameters only. | [optional]
**utm** | Option<[**models::StoredEventUtm**](StoredEventUtm.md)> |  | [optional]
**zrn** | Option<**String**> |  | [optional]
**click_ids** | Option<[**models::StoredEventClickIds**](StoredEventClickIds.md)> |  | [optional]
**destinations_sent** | Option<**i32**> |  | [optional]
**has_email** | Option<**bool**> |  | [optional]
**has_phone** | Option<**bool**> |  | [optional]
**has_external_id** | Option<**bool**> |  | [optional]
**campaign** | [**models::WebhookPayloadConversionConversionCampaign**](WebhookPayloadConversionConversionCampaign.md) |  | 
**campaign_match** | **String** | `matched`, or why there is no campaign: `no_hint`, `no_campaign`, `ambiguous`, `not_counted` or `match_failed`. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


