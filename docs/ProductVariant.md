# ProductVariant

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Platform-native variant id (numeric string for Shopify). | [optional]
**title** | Option<**String**> | Option combination label, e.g. \"S / Blue\". | [optional]
**sku** | Option<**String**> |  | [optional]
**barcode** | Option<**String**> |  | [optional]
**price** | Option<**String**> | Decimal amount in the store currency, e.g. \"19.90\". | [optional]
**compare_at_price** | Option<**String**> | Strike-through price; null when the variant is not on sale. | [optional]
**inventory_quantity** | Option<**i32**> | Units on hand across locations; null when inventory is not tracked. | [optional]
**available_for_sale** | Option<**bool**> |  | [optional]
**selected_options** | Option<[**Vec<models::ProductVariantSelectedOptionsInner>**](ProductVariantSelectedOptionsInner.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


