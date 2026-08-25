# SendInboxMessageRequestInteractiveActionOneOf10Parameters

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**country** | **String** | ISO 3166-1 alpha-2 country code Meta should localize the address form for (e.g. IN). Required: Meta rejects the send without it. | 
**values** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Optional pre-filled address field values. | [optional]
**saved_addresses** | Option<**Vec<std::collections::HashMap<String, serde_json::Value>>**> | Optional list of the recipient's previously saved addresses to offer as quick picks. | [optional]
**validation_errors** | Option<**std::collections::HashMap<String, String>**> | Optional per-field error messages to show when re-prompting after a failed validation. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


