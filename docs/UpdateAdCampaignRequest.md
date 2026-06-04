# UpdateAdCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **Platform** |  (enum: facebook, instagram) | 
**budget** | Option<[**models::UpdateAdCampaignRequestBudget**](UpdateAdCampaignRequestBudget.md)> |  | [optional]
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> | Campaign-level default. Ad sets inherit this unless they override. | [optional]
**name** | Option<**String**> | Rename the campaign (Meta only; other platforms return 501). At least one of budget/bidStrategy/name is required. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


