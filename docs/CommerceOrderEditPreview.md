# CommerceOrderEditPreview

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**subtotal** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**total** | Option<[**models::CommerceMoney**](CommerceMoney.md)> |  | [optional]
**outstanding** | Option<[**models::CommerceMoney**](CommerceMoney.md)> | What the buyer still owes. Negative when the edit leaves them overpaid: refund that with the refunds endpoint. | [optional]
**line_items** | Option<[**Vec<models::CommerceOrderEditPreviewLineItemsInner>**](CommerceOrderEditPreviewLineItemsInner.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


