# CreateStandaloneAdRequestPromotedObject

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pixel_id** | Option<**String**> | Pixel ID. **Meta:** Facebook Pixel ID, required for `goal: conversions`. **TikTok:** TikTok Pixel ID, required for `goal: conversions`.  | [optional]
**custom_event_type** | Option<**String**> | The event the campaign/ad group optimises against.  **Meta:** standard event like `PURCHASE`, `LEAD`, `COMPLETE_REGISTRATION`, `ADD_TO_CART`. Uppercased internally so callers can pass any case. Required for `goal: conversions`.  **TikTok:** an `optimization_event` code (UPPER_SNAKE, not Meta's vocabulary and not PascalCase). Must be one of the event types your TikTok Pixel is configured to track; passed through verbatim and validated by TikTok. Newer pixels (Events API / funnel-template setups) use TikTok's updated taxonomy, e.g. `SHOPPING` for purchase/payment events; legacy pixels use codes like `ON_WEB_ORDER` (Complete Payment), `INITIATE_ORDER` (Place an Order), `ON_WEB_CART` (Add to Cart), `ON_WEB_REGISTER` (Complete Registration), `FORM` (Submit Form), `ON_WEB_DETAIL` (View Content). On rejection the error lists the event types your pixel actually tracks. Optional for `goal: conversions`.  | [optional]
**page_id** | Option<**String**> | Facebook Page ID. Used by `goal: lead_generation`. Auto-filled from the connected Page when omitted.  | [optional]
**application_id** | Option<**String**> | App ID. Required for `goal: app_promotion`. | [optional]
**object_store_url** | Option<**String**> | App Store / Play Store listing URL. Required for `goal: app_promotion`. | [optional]
**custom_conversion_id** | Option<**String**> | Custom Conversion ID, when optimising against one instead of a standard event. | [optional]
**product_catalog_id** | Option<**String**> | Catalog ID for catalog/Advantage+ Shopping campaigns. | [optional]
**product_set_id** | Option<**String**> | Product Set ID inside the catalog. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


