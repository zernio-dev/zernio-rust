# CreateCustomConversionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_account_id** | **String** | Meta ad account id (act_<n>). | 
**name** | **String** | Also the reuse key, together with pixelId. | 
**pixel_id** | **String** | Meta pixel id (event_source_id). From GET /v1/accounts/{accountId}/tracking-tags. | 
**custom_event_type** | **String** | Meta custom_event_type, e.g. LEAD, PURCHASE, OTHER. | 
**rule** | **serde_json::Value** | Meta conversion rule, forwarded verbatim. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


