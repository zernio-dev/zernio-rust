# SendConversionsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | SocialAccount ID (metaads or googleads). | 
**destination_id** | **String** | Platform destination identifier. For Meta, the pixel/dataset ID. For Google, the conversion action resource name.  | 
**events** | [**Vec<models::ConversionEvent>**](ConversionEvent.md) |  | 
**test_code** | Option<**String**> | Meta `test_event_code` passthrough. Ignored by Google. | [optional]
**consent** | Option<[**models::SendConversionsRequestConsent**](SendConversionsRequestConsent.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


