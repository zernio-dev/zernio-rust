# CreateAdAccount201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_account_id** | **String** | New Meta ad account ID for subsequent ads calls. | 
**business_id** | **String** | Owning business portfolio ID. | 
**connection_updated** | **bool** | Whether the connection scope and discovery schedule were updated. | 
**payment_method_required** | **bool** | Always true as a delivery prerequisite. This is not a live funding-source check. Confirm payment or invoicing in Ads Manager. | 
**ads_manager_url** | **String** | Open the created account in Ads Manager. | 
**next_steps** | **String** | Payment setup instructions for the user. | 
**warnings** | **Vec<String>** | Recovery instructions if the account could not be attached to the connection. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


