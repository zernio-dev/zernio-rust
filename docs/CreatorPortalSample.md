# CreatorPortalSample

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**product_id** | **String** |  | 
**product_title** | **String** |  | 
**variant_title** | Option<**String**> |  | 
**status** | **Status** |  (enum: pending, approved, shipped, declined) | 
**shipping_address** | [**models::CampaignSampleShippingAddress**](CampaignSampleShippingAddress.md) |  | 
**note** | Option<**String**> |  | 
**discount_code** | Option<**String**> | The single-use code to redeem the product at checkout, once approved. | 
**tracking_url** | Option<**String**> |  | 
**decline_reason** | Option<**String**> |  | 
**requested_at** | **String** |  | 
**content_due_at** | Option<**String**> | When a post is due for the sample; null until approved. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


