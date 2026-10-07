# CreateSharedBudgetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Google ads SocialAccount id. | 
**ad_account_id** | Option<**String**> | Platform ad account ID (Google customer ID, digits only). Defaults to the account's connected customer. | [optional]
**name** | **String** |  | 
**amount** | **f64** | Daily amount in the account's currency units. | 
**r#type** | Option<**Type**> | Only daily is accepted (lifetime returns 422). (enum: daily, lifetime) | [optional][default to Daily]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


