# GetAdAccountLiveEntities200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> |  | [optional]
**ad_account_id** | Option<**String**> |  | [optional]
**platform** | Option<**Platform**> |  (enum: facebook, tiktok) | [optional]
**currency** | Option<**String**> | ISO 4217 code every budget and bid amount is expressed in. | [optional]
**read_at** | Option<**String**> | When the platform was read. | [optional]
**campaigns** | Option<[**Vec<models::GetAdAccountLiveEntities200ResponseCampaignsInner>**](GetAdAccountLiveEntities200ResponseCampaignsInner.md)> | Absent when `level=adSet`. | [optional]
**ad_sets** | Option<[**Vec<models::GetAdAccountLiveEntities200ResponseAdSetsInner>**](GetAdAccountLiveEntities200ResponseAdSetsInner.md)> | Absent when `level=campaign`. | [optional]
**paging** | Option<[**models::GetAdAccountLiveEntities200ResponsePaging**](GetAdAccountLiveEntities200ResponsePaging.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


