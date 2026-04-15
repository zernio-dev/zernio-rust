# ConversionEvent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**event_name** | **String** | Standard event name (Purchase, Lead, CompleteRegistration, AddToCart, InitiateCheckout, AddPaymentInfo, Subscribe, StartTrial, ViewContent, Search, Contact, SubmitApplication, Schedule) or a custom string (only supported on platforms that accept custom events).  | 
**event_time** | **i32** | When the conversion happened, in unix seconds. | 
**event_id** | **String** | Unique dedup key. The same eventId must be used on pixel + CAPI to prevent double-counting. Mapped to event_id on Meta and transactionId on Google.  | 
**value** | Option<**f64**> | Conversion value in the specified currency. | [optional]
**currency** | Option<**String**> | ISO 4217 currency code. | [optional]
**user** | [**models::ConversionEventUser**](ConversionEventUser.md) |  | 
**items** | Option<[**Vec<models::ConversionEventItemsInner>**](ConversionEventItemsInner.md)> | Item-level detail for ecommerce events. | [optional]
**source_url** | Option<**String**> | URL where the conversion originated (used by Meta). | [optional]
**action_source** | Option<**ActionSource**> | Where the conversion happened. Used by Meta; Google ignores. (enum: web, app, offline, crm, phone_call, system_generated) | [optional]
**platform_data** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Escape hatch for platform-specific fields we haven't normalized. Forwarded as-is. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


