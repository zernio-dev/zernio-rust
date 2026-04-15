# ConversionEventUser

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | Option<**String**> | Plaintext email. Hashed server-side. | [optional]
**phone** | Option<**String**> | Phone number, ideally E.164. Hashed server-side. | [optional]
**first_name** | Option<**String**> | Plaintext first name. Hashed server-side. | [optional]
**last_name** | Option<**String**> | Plaintext last name. Hashed server-side. | [optional]
**external_id** | Option<**String**> | Stable customer identifier (e.g. CRM user ID). Hashed server-side. | [optional]
**ip_address** | Option<**String**> | Client IP address. Sent plaintext. | [optional]
**user_agent** | Option<**String**> | Client user-agent string. Sent plaintext. | [optional]
**country** | Option<**String**> | ISO 3166-1 alpha-2 country code, e.g. 'us'. | [optional]
**click_ids** | Option<[**models::ConversionEventUserClickIds**](ConversionEventUserClickIds.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


