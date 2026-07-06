# GetCallsUsage200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**since** | Option<**String**> |  | [optional]
**until** | Option<**String**> |  | [optional]
**group_by** | Option<**GroupBy**> |  (enum: day, number, channel, ) | [optional]
**totals** | Option<[**models::GetCallsUsage200ResponseTotals**](GetCallsUsage200ResponseTotals.md)> |  | [optional]
**groups** | Option<[**Vec<models::GetCallsUsage200ResponseGroupsInner>**](GetCallsUsage200ResponseGroupsInner.md)> | Present (possibly empty) when `groupBy` is set. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


