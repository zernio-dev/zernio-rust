# SetUpAdAccountBillingRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Google ads SocialAccount id. | 
**ad_account_id** | **String** | Google Ads customer id to bill, digits only. | 
**payments_account_id** | **String** | Monthly invoicing payments account from GET /v1/ads/accounts/billing. | 
**spending_limit** | Option<**f64**> | Account budget cap in the account currency. Omit for an unlimited budget. | [optional]
**budget_name** | Option<**String**> |  | [optional][default to Zernio account budget]
**purchase_order_number** | Option<**String**> | Printed on the invoice. No effect on delivery. | [optional]
**validate_only** | Option<**bool**> |  | [optional][default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


