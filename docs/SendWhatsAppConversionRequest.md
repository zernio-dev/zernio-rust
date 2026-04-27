# SendWhatsAppConversionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp SocialAccount ID. | 
**event_name** | **EventName** | Live-verified allowlist of event names accepted by Meta's CAPI for Business Messaging (Graph API v25.0). Other standard pixel events including `Lead`, `CompleteRegistration`, `Subscribe`, `Schedule`, `Contact`, `StartTrial`, `AddPaymentInfo`, `Search`, and `SubmitApplication` are rejected with subcode 2804066 (\"Messaging Event Invalid Event Type\") on `action_source = business_messaging` events. Custom event names are also rejected.  Use `LeadSubmitted` (NOT `Lead`) for lead-style conversions.  (enum: LeadSubmitted, Purchase, AddToCart, InitiateCheckout, ViewContent) | 
**event_time** | Option<**f64**> | Unix seconds. Defaults to the time of the request when omitted. Meta's attribution window is 7 days from click; events older than that lose attribution.  | [optional]
**event_id** | **String** | Stable dedup key. Reuse to suppress duplicate events (Meta dedupes against pixel events with the same id).  | 
**conversation_id** | Option<**String**> | Zernio Conversation `_id` (preferred lookup). The conversation must have a captured `ctwa_clid` in metadata (set automatically by the WhatsApp webhook on the first inbound message after a CTWA ad click).  | [optional]
**phone_e164** | Option<**String**> | Contact phone number, digits only with no '+'. When used in lieu of `conversationId`, the handler resolves to the most recent CTWA-attributed conversation for this phone on the supplied account.  | [optional]
**value** | Option<**f64**> | Conversion value (e.g. order total). | [optional]
**currency** | Option<**String**> | ISO 4217 currency code (e.g. `USD`). | [optional]
**content_ids** | Option<**Vec<String>**> | Optional product / content identifiers. | [optional]
**email** | Option<**String**> | User email. Normalized + SHA-256 hashed before sending to Meta. | [optional]
**external_id** | Option<**String**> | Stable customer identifier. Lowercased + SHA-256 hashed before sending to Meta.  | [optional]
**test_code** | Option<**String**> | Meta `test_event_code` passthrough. Routes the event to the Test Events tab in Events Manager instead of the production dataset, useful for development.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


