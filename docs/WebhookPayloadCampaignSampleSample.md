# WebhookPayloadCampaignSampleSample

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**store_account_id** | **String** |  | 
**product_id** | **String** |  | 
**variant_id** | Option<**String**> |  | 
**product_title** | **String** |  | 
**variant_title** | Option<**String**> |  | 
**status** | **Status** |  (enum: pending, approved, shipped, declined) | 
**shipping_address** | [**models::CampaignSampleShippingAddress**](CampaignSampleShippingAddress.md) |  | 
**note** | Option<**String**> |  | 
**discount_code** | Option<**String**> | The 100%-off, single-use code, set from approval on. | 
**tracking_url** | Option<**String**> |  | 
**decline_reason** | Option<**String**> |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


