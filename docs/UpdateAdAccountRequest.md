# UpdateAdAccountRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Account ID (metaads, or a facebook/instagram posting account) | 
**ad_account_id** | **String** | Meta ad account ID (act_...) | 
**name** | Option<**String**> | New ad account name. | [optional]
**spend_cap** | Option<**f64**> | Account spend cap in whole currency units; null removes it. | [optional]
**reset_amount_spent** | Option<**bool**> | Restart the amount counted against the cap from zero. Cannot be combined with spendCap null. | [optional]
**default_dsa_beneficiary** | Option<**String**> | Legal entity benefiting from ads on this ad account | [optional]
**default_dsa_payor** | Option<**String**> | Legal entity paying for ads on this ad account. Defaults to defaultDsaBeneficiary when omitted. Requires defaultDsaBeneficiary. | [optional]
**tracking_url_template** | Option<**String**> | **Google only.** Account tracking template (customer.tracking_url_template); an empty string clears it. | [optional]
**final_url_suffix** | Option<**String**> | **Google only.** Account final URL suffix (customer.final_url_suffix); an empty string clears it. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


