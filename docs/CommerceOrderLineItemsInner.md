# CommerceOrderLineItemsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**product_id** | Option<**String**> | Null when the product was deleted. | [optional]
**variant_id** | Option<**String**> |  | [optional]
**sku** | Option<**String**> |  | [optional]
**title** | Option<**String**> |  | [optional]
**variant_title** | Option<**String**> |  | [optional]
**quantity** | Option<**i32**> | As ordered; refunded units are listed under refunds. | [optional]
**unit_price** | Option<[**models::CommerceMoney**](CommerceMoney.md)> | Before discounts. | [optional]
**subtotal** | Option<[**models::CommerceMoney**](CommerceMoney.md)> | unitPrice x quantity. | [optional]
**discount_total** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**total** | Option<[**models::CommerceMoney**](CommerceMoney.md)> | subtotal minus discountTotal. | [optional]
**tax_lines** | Option<[**Vec<models::CommerceTaxLine>**](CommerceTaxLine.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


