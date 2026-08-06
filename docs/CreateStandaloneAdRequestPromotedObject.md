# CreateStandaloneAdRequestPromotedObject

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pixel_id** | Option<**String**> | Pixel ID. **Meta:** Facebook Pixel ID, required for `goal: conversions`. **TikTok:** TikTok Pixel ID, required for `goal: conversions`. To discover the pixels an ad account can use, call `GET /v1/accounts/{accountId}/tracking-tags?adAccountId=act_...` (each entry carries `kind` and `ownerAdAccountId`), or `GET /v1/accounts/{accountId}/conversion-destinations`. Note this is a different resource from `GET /v1/ads/{adId}/tracking-tags`, which reads an ad's click-URL params (`url_tags`), not pixels.  | [optional]
**custom_event_type** | Option<**String**> | The event the campaign/ad group optimises against.  **Meta:** standard event like `PURCHASE`, `LEAD`, `COMPLETE_REGISTRATION`, `ADD_TO_CART`. Uppercased internally so callers can pass any case. Required for `goal: conversions`.  **TikTok:** an `optimization_event` code (UPPER_SNAKE, not Meta's vocabulary and not PascalCase), OR the exact event name shown in TikTok Events Manager (auto-resolved to its code). Must be one of the event types your TikTok Pixel tracks; custom events are not optimizable. Current taxonomy: `SHOPPING` (Purchase), `ON_WEB_CART` (Add to Cart), `INITIATE_ORDER` (Initiate Checkout), `FORM` (Lead), `ON_WEB_REGISTER` (Complete Registration), `ON_WEB_DETAIL` (View Content). `ON_WEB_ORDER` is deprecated. On rejection the error lists the event types your pixel actually tracks. Optional for `goal: conversions`.  | [optional]
**custom_event_str** | Option<**String**> | Meta only. Pixel custom-event name to optimise against (Meta's `custom_event_str`), exactly as it appears in Events Manager and in your CAPI payloads (case-sensitive, not uppercased). Requires `customEventType: OTHER`, and `OTHER` requires this field (400 either way). The same as picking a custom event in Ads Manager's conversion-event dropdown. For rule-based Custom Conversions use `customConversionId` instead.  | [optional]
**page_id** | Option<**String**> | Facebook Page ID. Used by `goal: lead_generation`. Auto-filled from the connected Page when omitted.  | [optional]
**application_id** | Option<**String**> | App ID. Required for `goal: app_promotion`. | [optional]
**object_store_url** | Option<**String**> | App Store / Play Store listing URL. Required for `goal: app_promotion`. | [optional]
**custom_conversion_id** | Option<**String**> | Custom Conversion ID, when optimising against one instead of a standard event. | [optional]
**product_catalog_id** | Option<**String**> | Catalog ID for catalog/Advantage+ Shopping campaigns. | [optional]
**product_set_id** | Option<**String**> | Product Set ID inside the catalog. | [optional]
**offline_conversion_data_set_id** | Option<**String**> | Meta only. Offline event set (dataset) to optimise toward. Post-merger these are datasets: the id is the dataset id (for pixel-backed datasets, the pixel id). | [optional]
**whatsapp_phone_number** | Option<**String**> | Meta only. WhatsApp number on messaging-destination ad sets. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


