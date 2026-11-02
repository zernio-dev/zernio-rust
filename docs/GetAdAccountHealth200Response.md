# GetAdAccountHealth200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_account_id** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: ok, attention, blocked) | [optional]
**ready** | Option<**bool**> | False when a create or boost on this ad account would be refused; `blockers` says why. | [optional]
**blockers** | Option<[**Vec<models::GetAdAccountHealth200ResponseBlockersInner>**](GetAdAccountHealth200ResponseBlockersInner.md)> |  | [optional]
**checked_at** | Option<**String**> |  | [optional]
**checks** | Option<[**Vec<models::GetAdAccountHealth200ResponseChecksInner>**](GetAdAccountHealth200ResponseChecksInner.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


