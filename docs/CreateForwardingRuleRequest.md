# CreateForwardingRuleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**account_id** | **String** | Connected ads account ID that owns the destination. | 
**destination_id** | **String** | The platform destination: a pixel, a conversion action or a conversion rule. | 
**event_names** | Option<**Vec<String>**> |  | [optional]
**sources** | Option<**Vec<Sources>**> | Forward only events from these sources, such as only `web` for a tracked website. Leave it out to forward events from every source. (enum: api, relay, hubspot, meta_leads, google_leads, linkedin_leads, tiktok_leads, shopify, woocommerce, stripe, web) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


