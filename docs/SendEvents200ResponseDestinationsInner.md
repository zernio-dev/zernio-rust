# SendEvents200ResponseDestinationsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> |  | [optional]
**destination_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: metaads, googleads, linkedinads, tiktokads, openaiads, pinterestads, redditads) | [optional]
**events_sent** | Option<**i32**> | Events the platform accepted. | [optional]
**events_failed** | Option<**i32**> |  | [optional]
**failures** | Option<[**Vec<models::SendEvents200ResponseDestinationsInnerFailuresInner>**](SendEvents200ResponseDestinationsInnerFailuresInner.md)> |  | [optional]
**error** | Option<**String**> | Set when the destination could not be reached at all (account disconnected, unsupported platform, platform error). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


