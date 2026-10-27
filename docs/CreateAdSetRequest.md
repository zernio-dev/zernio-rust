# CreateAdSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id owning the Google Ads or Reddit Ads connection. | 
**platform** | **Platform** | \"google\" and \"reddit\" are implemented; every other value returns 501. (enum: facebook, instagram, tiktok, linkedin, pinterest, google, twitter, openai, reddit) | 
**campaign_id** | **String** | Platform campaign ID the ad group is created under (numeric on Google). | 
**name** | **String** |  | 
**status** | Option<**Status**> |  (enum: ACTIVE, PAUSED) | [optional][default to Paused]
**max_cpc** | Option<**f64**> | Max CPC of the new ad group, in the account's currency units. Send it when the campaign uses Manual CPC: Google gives an ad group without one a 0.01 bid. | [optional]
**ad_account_id** | Option<**String**> | Platform ad account ID: the Google customer ID (digits only, only required when the connection has more than one) or the Reddit ad account id (required). | [optional]
**customer_id** | Option<**String**> | Google only. Alias of adAccountId, kept for existing callers | [optional]
**budget_amount** | Option<**f64**> | Reddit only. Budget of the new ad group, in the ad account's currency units. Required when the campaign has no campaign budget; not applied under campaign budget optimization. | [optional]
**budget_type** | Option<**BudgetType**> | Reddit only. Sent together with budgetAmount. (enum: daily, lifetime) | [optional]
**start_date** | Option<**String**> | Reddit only. ISO 8601 start of the ad group. Defaults to now, or to the campaign start when it is in the future. | [optional]
**end_date** | Option<**String**> | Reddit only. ISO 8601 end of the ad group. Defaults to the campaign end. | [optional]
**targeting** | Option<[**models::TargetingSpec**](TargetingSpec.md)> |  | [optional]
**promoted_object** | Option<[**models::CreateAdSetRequestPromotedObject**](CreateAdSetRequestPromotedObject.md)> |  | [optional]
**optimization_goal** | Option<**String**> | Reddit only. VIDEO_VIEW_6S (default) or VIDEO_VIEW_15S on a video views campaign. | [optional]
**bid_strategy** | Option<**BidStrategy**> | Reddit only. Defaults to LOWEST_COST_WITHOUT_CAP. Not accepted under campaign budget optimization. (enum: LOWEST_COST_WITHOUT_CAP, LOWEST_COST_WITH_BID_CAP, COST_CAP) | [optional]
**bid_amount** | Option<**f64**> | Reddit only. Bid cap in currency units, sent with bidStrategy. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


