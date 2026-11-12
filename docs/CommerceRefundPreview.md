# CommerceRefundPreview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**amount** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**maximum_refundable** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**subtotal** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**tax** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**shipping** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**line_items** | Option<[**Vec<models::CommerceRefundPreviewLineItemsInner>**](CommerceRefundPreviewLineItemsInner.md)> |  | [optional]
**transactions** | Option<[**Vec<models::CommerceRefundPreviewTransactionsInner>**](CommerceRefundPreviewTransactionsInner.md)> | The payments the money goes back to. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


