# WebhookPayloadAccountPrivacyRequestPrivacyRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** | customer_data_request: the merchant asked for the data you hold about `customer`. Send it to the merchant.  customer_redact: erase the data you hold about `customer` and the orders in `orderIds`.  shop_redact: erase the data you hold about the whole shop. Sent 48 hours after the merchant uninstalled the app. (enum: customer_data_request, customer_redact, shop_redact) | 
**shop_domain** | **String** |  | 
**shop_id** | Option<**String**> |  | 
**customer** | [**models::WebhookPayloadAccountPrivacyRequestPrivacyRequestCustomer**](WebhookPayloadAccountPrivacyRequestPrivacyRequestCustomer.md) |  | 
**order_ids** | **Vec<String>** | The Shopify order ids the request covers. Empty for shop_redact. | 
**data_request_id** | Option<**String**> | Shopify's id for a customer_data_request. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


