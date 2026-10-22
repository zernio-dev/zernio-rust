# CommerceOrder

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: shopify, woocommerce) | [optional]
**number** | Option<**String**> | The number the merchant and buyer see. | [optional]
**status** | Option<[**models::CommerceOrderStatus**](CommerceOrderStatus.md)> |  | [optional]
**platform_status** | Option<**String**> | Shopify fulfilment status (e.g. UNFULFILLED) or WooCommerce order status (e.g. processing). | [optional]
**payment_status** | Option<**PaymentStatus**> |  (enum: pending, authorized, partially_paid, paid, partially_refunded, refunded, voided, failed) | [optional]
**platform_payment_status** | Option<**String**> | Shopify financial status. Null on WooCommerce, where payment is read from the order status. | [optional]
**currency** | Option<**String**> |  | [optional]
**taxes_included** | Option<**bool**> | Whether line item and shipping amounts include tax. Always false on WooCommerce, whose API returns amounts before tax whatever the store displays (platformData.pricesIncludeTax). | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]
**paid_at** | Option<**String**> | WooCommerce only; null on Shopify. | [optional]
**cancelled_at** | Option<**String**> | Shopify only; null on WooCommerce. | [optional]
**cancel_reason** | Option<**String**> |  | [optional]
**subtotal** | Option<[**models::CommerceMoney**](CommerceMoney.md)> | Line items before order discounts and shipping. | [optional]
**discount_total** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**shipping_total** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**tax_total** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**total** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**refunded_total** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**discount_codes** | Option<**Vec<String>**> |  | [optional]
**payment_methods** | Option<**Vec<String>**> |  | [optional]
**customer** | Option<[**models::CommerceOrderCustomer**](CommerceOrderCustomer.md)> |  | [optional]
**billing_address** | Option<[**models::CommerceAddress**](CommerceAddress.md)> |  | [optional]
**shipping_address** | Option<[**models::CommerceAddress**](CommerceAddress.md)> |  | [optional]
**buyer_note** | Option<**String**> |  | [optional]
**attribution** | Option<[**models::CommerceOrderAttribution**](CommerceOrderAttribution.md)> |  | [optional]
**line_items** | Option<[**Vec<models::CommerceOrderLineItemsInner>**](CommerceOrderLineItemsInner.md)> |  | [optional]
**shipping_lines** | Option<[**Vec<models::CommerceOrderChargeLine>**](CommerceOrderChargeLine.md)> |  | [optional]
**fee_lines** | Option<[**Vec<models::CommerceOrderChargeLine>**](CommerceOrderChargeLine.md)> | WooCommerce fees. Always empty on Shopify. | [optional]
**tax_lines** | Option<[**Vec<models::CommerceTaxLine>**](CommerceTaxLine.md)> | Order tax by rate, line items and shipping together. | [optional]
**refunds** | Option<[**Vec<models::CommerceOrderRefundsInner>**](CommerceOrderRefundsInner.md)> |  | [optional]
**fulfillments** | Option<[**Vec<models::CommerceOrderFulfillmentsInner>**](CommerceOrderFulfillmentsInner.md)> |  | [optional]
**platform_data** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Platform-only fields. Null when the platform has none. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


