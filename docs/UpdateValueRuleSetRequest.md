# UpdateValueRuleSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id (posting or ads variant) used to resolve the Meta token. | 
**name** | **String** | Required: the update replaces the whole set. | 
**rules** | [**Vec<models::ValueRule>**](ValueRule.md) | The COMPLETE rule list. Omitting a rule deletes it on Meta. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


