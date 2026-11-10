# ListCampaignOrders200ResponseOrdersInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**platform_order_id** | **String** | The order id on the store, as in `GET /v1/commerce/orders/{orderId}`. | 
**order_number** | **String** |  | 
**status** | **Status** |  (enum: pending, matched, unmatched) | 
**participant_id** | Option<**String**> |  | 
**creator_name** | Option<**String**> |  | 
**creator_avatar_url** | Option<**String**> | The creator's profile picture. Same source as a participant's `creator.avatarUrl`. | 
**matched_by** | Option<**MatchedBy**> |  (enum: code, link, ) | 
**discount_code** | Option<**String**> |  | 
**currency** | **String** |  | 
**sales_cents** | **i32** |  | 
**refunded_cents** | **i32** |  | 
**commission_cents** | **i32** | Commission the order holds now, net of refunds. | 
**order_created_at** | **String** |  | 
**approved_at** | Option<**String**> |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


