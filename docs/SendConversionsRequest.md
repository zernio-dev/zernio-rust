# SendConversionsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | SocialAccount ID (metaads, googleads, linkedinads, tiktokads, openaiads, pinterestads, or redditads). | 
**destination_id** | **String** | Platform destination identifier. For Meta, the pixel/dataset ID. For Google, the conversion action resource name. For LinkedIn, the conversion rule ID or full `urn:lla:llaPartnerConversion:{id}` URN. For OpenAI Ads, the pixel wire id. For Pinterest, the numeric ad account id. For Reddit, the pixel id (`a2_...`).  | 
**events** | [**Vec<models::ConversionEvent>**](ConversionEvent.md) |  | 
**test_code** | Option<**String**> | Meta `test_event_code` passthrough. On Pinterest any value sends the batch with `test=true` (validated, not recorded). On Reddit, sent as `test_id` so the events show in the pixel's test view. Ignored by Google, LinkedIn, and OpenAI Ads. | [optional]
**consent** | Option<[**models::SendConversionsRequestConsent**](SendConversionsRequestConsent.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


