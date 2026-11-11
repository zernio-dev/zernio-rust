# ForwardingRule

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Rule ID, used to delete it. | [optional]
**profile_id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**destination_id** | Option<**String**> | Platform destination (pixel, conversion action, rule, ...). | [optional]
**event_names** | Option<**Vec<String>**> | Event names forwarded to this destination; null forwards every event. | [optional]
**sources** | Option<**Vec<Sources>**> | Event sources forwarded to this destination; null forwards events from every source. (enum: api, relay, hubspot, meta_leads, google_leads, linkedin_leads, tiktok_leads, shopify, woocommerce, stripe, web) | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


