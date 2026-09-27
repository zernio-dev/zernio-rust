# GooglePmaxAssetGroup

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Stable Google asset group id. Use it in the asset-group endpoints below. | 
**resource_name** | **String** | customers/{customerId}/assetGroups/{assetGroupId} | 
**campaign_id** | **String** |  | 
**name** | **String** |  | 
**status** | **String** | Asset-group status on Google. Campaign status independently controls delivery. | 
**final_urls** | **Vec<String>** |  | 
**final_mobile_urls** | **Vec<String>** |  | 
**path1** | Option<**String**> |  | 
**path2** | Option<**String**> |  | 
**ad_strength** | Option<**String**> | Google ad strength, such as POOR, AVERAGE, GOOD or EXCELLENT. | 
**primary_status** | Option<**String**> | Why the group is or is not serving, such as ELIGIBLE, PAUSED or NOT_ELIGIBLE. | 
**primary_status_reasons** | **Vec<String>** |  | 
**assets** | [**Vec<models::GooglePmaxAssetGroupAssetsInner>**](GooglePmaxAssetGroupAssetsInner.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


