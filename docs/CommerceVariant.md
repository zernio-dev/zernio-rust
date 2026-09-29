# CommerceVariant

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Platform-native variant id. | [optional]
**title** | Option<**String**> | Option combination label, e.g. \"S / Blue\". | [optional]
**sku** | Option<**String**> |  | [optional]
**barcode** | Option<**String**> |  | [optional]
**price** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**compare_at_price** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**inventory_quantity** | Option<**i32**> | Units on hand; null when inventory is not tracked. | [optional]
**available_for_sale** | Option<**bool**> |  | [optional]
**options** | Option<[**Vec<models::CreateCommerceProductVariantsRequestVariantsInnerOptionsInner>**](CreateCommerceProductVariantsRequestVariantsInnerOptionsInner.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


