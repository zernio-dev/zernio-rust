# CreateCommerceOrderEditRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | 
**add** | Option<[**Vec<models::CreateCommerceOrderEditRequestAddInner>**](CreateCommerceOrderEditRequestAddInner.md)> |  | [optional]
**quantities** | Option<[**Vec<models::CreateCommerceOrderEditRequestQuantitiesInner>**](CreateCommerceOrderEditRequestQuantitiesInner.md)> |  | [optional]
**notify_customer** | Option<**bool**> |  | [optional][default to false]
**staff_note** | Option<**String**> |  | [optional]
**validate_only** | Option<**bool**> | Return the edited totals without changing the order. | [optional][default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


