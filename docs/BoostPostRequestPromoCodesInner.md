# BoostPostRequestPromoCodesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**discount_type** | **DiscountType** |  (enum: PERCENTAGE, CASH) | 
**discount_value** | **f64** | PERCENTAGE: integer 1-100. CASH: amount greater than 0 in discountCurrency. | 
**discount_currency** | Option<**String**> | ISO 4217; required for CASH. | [optional]
**promo_code** | Option<**String**> | Code entered at checkout; omit for an automatic offer. | [optional]
**minimum_purchase_type** | Option<**MinimumPurchaseType**> |  (enum: QUANTITY, SUBTOTAL) | [optional]
**minimum_purchase_value** | Option<**f64**> | Required with minimumPurchaseType; QUANTITY is an integer >= 0, SUBTOTAL an amount > 0. | [optional]
**minimum_purchase_currency** | Option<**String**> | ISO 4217; required for SUBTOTAL. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


