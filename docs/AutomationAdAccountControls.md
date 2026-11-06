# AutomationAdAccountControls

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> | The connection your automations reach the ad account through; null when no automation uses it any more. | 
**platform** | **String** | The ad platform, for example `facebook`. | 
**ad_account_id** | **String** | The platform's ad account id. | 
**paused** | **bool** | True when every ad rule on this ad account is stopped. | 
**paused_at** | Option<**String**> |  | 
**daily_raise_limit** | Option<**f64**> | The most automations may raise budgets on this ad account in any 24 hours, in the ad account's currency. Null when there is no limit. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


