# CreateCommerceRefundRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | 
**line_items** | Option<[**Vec<models::CommerceRefundRequestLineItemsInner>**](CommerceRefundRequestLineItemsInner.md)> |  | [optional]
**shipping** | Option<[**models::CommerceRefundRequestShipping**](CommerceRefundRequestShipping.md)> |  | [optional]
**amount** | Option<**String**> | Refund this much money instead of what the lines and shipping are worth, for a goodwill refund or a partial one. Taken from the order's payments in order, up to what each can still refund. | [optional]
**currency** | Option<**String**> | The currency your amounts are in. Refused (400) unless it is the one the buyer paid in, which every refund amount uses. | [optional]
**note** | Option<**String**> | Kept on the refund, visible to staff. | [optional]
**notify_customer** | Option<**bool**> | Email the buyer about the refund. | [optional][default to false]
**validate_only** | Option<**bool**> | Return the refund the platform would make, without refunding anything. | [optional][default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


