# CreateValueRuleSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant); its platform decides where the campaign is created. | 
**ad_account_id** | **String** | Platform ad account id (Meta act_<n>, Google customer id, LinkedIn account id, ...). | 
**name** | **String** |  | 
**rules** | [**Vec<models::ValueRule>**](ValueRule.md) | Evaluated in order; the first matching rule wins. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


