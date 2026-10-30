# UploadCampaignResultsRequestRowsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**date** | [**String**](String.md) | The day, at most 400 days ago. | 
**campaign_id** | Option<**String**> | The platform campaign id. | [optional]
**utm_campaign** | Option<**String**> | The `utm_campaign` value on the campaign's ads. | [optional]
**campaign_name** | Option<**String**> | The campaign's name, matched case-insensitively. | [optional]
**ad_account_id** | Option<**String**> | Platform ad account id. Narrows matching to one ad account. | [optional]
**values** | **std::collections::HashMap<String, f64>** | Metric key (snake_case, up to 40 characters) to a non-negative number. 1 to 20 per row. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


