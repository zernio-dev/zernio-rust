# CreateStandaloneAdRequestPromotedObject

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pixel_id** | Option<**String**> | Pixel ID. **Meta:** Facebook Pixel ID, required for `goal: conversions`. **TikTok:** TikTok Pixel ID, required for `goal: conversions`.  | [optional]
**custom_event_type** | Option<**String**> | The event the campaign/ad group optimises against.  **Meta:** standard event like `PURCHASE`, `LEAD`, `COMPLETE_REGISTRATION`, `ADD_TO_CART`. Uppercased internally so callers can pass any case. Required for `goal: conversions`.  **TikTok:** an `optimization_event` code (UPPER_SNAKE, not Meta's vocabulary and not PascalCase), e.g. `ON_WEB_ORDER` (Complete Payment), `INITIATE_ORDER` (Place an Order), `ON_WEB_CART` (Add to Cart), `ON_WEB_REGISTER` (Complete Registration), `FORM` (Submit Form), `ON_WEB_DETAIL` (View Content). Must be one of the events your TikTok Pixel is configured to track; passed through verbatim and validated by TikTok. Optional for `goal: conversions`.  | [optional]
**page_id** | Option<**String**> | Facebook Page ID. Used by `goal: lead_generation`. Auto-filled from the connected Page when omitted.  | [optional]
**application_id** | Option<**String**> | App ID. Required for `goal: app_promotion`. | [optional]
**object_store_url** | Option<**String**> | App Store / Play Store listing URL. Required for `goal: app_promotion`. | [optional]
**custom_conversion_id** | Option<**String**> | Custom Conversion ID, when optimising against one instead of a standard event. | [optional]
**product_catalog_id** | Option<**String**> | Catalog ID for catalog/Advantage+ Shopping campaigns. | [optional]
**product_set_id** | Option<**String**> | Product Set ID inside the catalog. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


