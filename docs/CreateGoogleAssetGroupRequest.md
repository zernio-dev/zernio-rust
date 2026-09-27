# CreateGoogleAssetGroupRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **String** | Unique within the campaign. | 
**final_urls** | **Vec<String>** |  | 
**final_mobile_urls** | Option<**Vec<String>**> |  | [optional]
**path1** | Option<**String**> |  | [optional]
**path2** | Option<**String**> | Requires path1. | [optional]
**status** | Option<**Status**> |  (enum: ENABLED, PAUSED) | [optional][default to Paused]
**assets** | Option<[**Vec<models::GoogleAssetGroupAssetLink>**](GoogleAssetGroupAssetLink.md)> |  | [optional]
**listing_group_filter** | Option<[**models::GoogleListingGroupTree**](GoogleListingGroupTree.md)> |  | [optional]
**validate_only** | Option<**bool**> |  | [optional][default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


