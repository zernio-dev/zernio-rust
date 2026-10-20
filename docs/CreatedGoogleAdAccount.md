# CreatedGoogleAdAccount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **Platform** |  (enum: google) | 
**ad_account_id** | **String** | New Google Ads customer id for subsequent ads calls. | 
**manager_customer_id** | **String** | Manager the account was created under. | 
**connection_updated** | **bool** | Whether the customer was added to the connection and discovery was scheduled. When false the account exists: reconnect Google Ads instead of creating it again. | 
**warnings** | **Vec<String>** | Recovery instructions if the account could not be attached to the connection. | 
**payment_method_required** | **bool** | Always true. The account has no billing until it is set up in Google Ads. | 
**next_steps** | **String** | Billing setup instructions for the user. | 
**validate_only** | **bool** | Always false on a 201. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


