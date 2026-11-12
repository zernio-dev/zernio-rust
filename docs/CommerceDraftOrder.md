# CommerceDraftOrder

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: shopify, woocommerce) | [optional]
**name** | Option<**String**> |  | [optional]
**status** | Option<**Status**> |  (enum: open, invoice_sent, completed) | [optional]
**invoice_url** | Option<**String**> | The checkout link the buyer pays through. | [optional]
**invoice_sent_at** | Option<**String**> |  | [optional]
**email** | Option<**String**> |  | [optional]
**customer_id** | Option<**String**> |  | [optional]
**note** | Option<**String**> |  | [optional]
**tags** | Option<**Vec<String>**> |  | [optional]
**currency** | Option<**String**> | The currency the buyer pays in; every amount uses it. | [optional]
**subtotal** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**discount_total** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**shipping_total** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**tax_total** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**total** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**line_items** | Option<[**Vec<models::CommerceDraftOrderLineItemsInner>**](CommerceDraftOrderLineItemsInner.md)> |  | [optional]
**shipping_address** | Option<[**models::CommerceAddress**](CommerceAddress.md)> |  | [optional]
**order_id** | Option<**String**> | The order it became once completed. | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]
**completed_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


