# GetSmsUsage200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**since** | Option<**String**> |  | [optional]
**until** | Option<**String**> |  | [optional]
**group_by** | Option<**GroupBy**> |  (enum: day, number, ) | [optional]
**totals** | Option<[**models::GetSmsUsage200ResponseTotals**](GetSmsUsage200ResponseTotals.md)> |  | [optional]
**groups** | Option<[**Vec<models::GetSmsUsage200ResponseGroupsInner>**](GetSmsUsage200ResponseGroupsInner.md)> | Present (possibly empty) when `groupBy` is set. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


