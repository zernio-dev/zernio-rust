# CreateForwardingRuleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**account_id** | **String** | Connected ads account ID that owns the destination. | 
**destination_id** | **String** | The platform destination: a pixel, a conversion action, a conversion rule, or a GA4 web stream measurement id (`G-…`). | 
**event_names** | Option<**Vec<String>**> |  | [optional]
**sources** | Option<**Vec<Sources>**> | Forward only events from these sources, such as only `web` for a tracked website. Leave it out to forward events from every source. (enum: api, relay, hubspot, meta_leads, google_leads, linkedin_leads, tiktok_leads, shopify, woocommerce, stripe, web) | [optional]
**api_secret** | Option<**String**> | Google Analytics streams only: the stream's Measurement Protocol API secret (GA4 Admin › Data streams). Optional when the connection has edit access, since Zernio then creates it. Checked against Google's validation server, stored encrypted, never returned. Change it with `PATCH /v1/events/forwarding-rules/{ruleId}`. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


