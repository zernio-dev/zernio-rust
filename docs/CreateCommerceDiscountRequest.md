# CreateCommerceDiscountRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**title** | **String** |  | 
**method** | **Method** |  (enum: code, automatic) | 
**r#type** | **Type** |  (enum: percentage, fixed_amount, free_shipping) | 
**code** | Option<**String**> | Required for method code. | [optional]
**percentage** | Option<**f64**> | For type percentage, e.g. 15 for 15%. | [optional]
**amount** | Option<**String**> | For type fixed_amount, a decimal in the store currency. | [optional]
**applies_on_each_item** | Option<**bool**> | fixed_amount only: take the amount off each item instead of once per order. | [optional]
**minimum_subtotal** | Option<**String**> | Minimum order subtotal, a decimal in the store currency. | [optional]
**minimum_quantity** | Option<**i32**> |  | [optional]
**usage_limit** | Option<**i32**> | Code discounts only: total uses allowed. | [optional]
**once_per_customer** | Option<**bool**> | Code discounts only. | [optional]
**starts_at** | Option<**String**> | Defaults to now. | [optional]
**ends_at** | Option<**String**> |  | [optional]
**product_ids** | Option<**Vec<String>**> |  | [optional]
**collection_ids** | Option<**Vec<String>**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


