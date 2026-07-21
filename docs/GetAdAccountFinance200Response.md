# GetAdAccountFinance200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_account_id** | Option<**String**> |  | [optional]
**currency** | Option<**String**> | ISO 4217 code all money values are expressed in. | [optional]
**balance** | Option<**f64**> | Outstanding/prepaid balance in whole currency units. | [optional]
**amount_spent** | Option<**f64**> | Lifetime amount spent in whole currency units. | [optional]
**spend_cap** | Option<**f64**> | Account spend cap; null when none is set. | [optional]
**funding_source** | Option<[**models::GetAdAccountFinance200ResponseFundingSource**](GetAdAccountFinance200ResponseFundingSource.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


