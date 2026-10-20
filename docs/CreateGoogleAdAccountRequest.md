# CreateGoogleAdAccountRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **Platform** |  (enum: google) | 
**account_id** | **String** | Zernio googleads SocialAccount ID whose Google user reaches the manager. | 
**manager_customer_id** | **String** | Manager (MCC) customer id without dashes. The new account is created under it. List reachable managers with GET /v1/ads/accounts/hierarchy. | 
**name** | **String** | Account name. Whitespace is trimmed. | 
**currency** | **String** | Uppercase ISO 4217 currency. Cannot be changed after creation. | 
**time_zone** | **String** | IANA time zone name, for example Europe/Madrid. Cannot be changed after creation. | 
**validate_only** | Option<**bool**> | Ask Google to validate the request without creating the account. | [optional][default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


