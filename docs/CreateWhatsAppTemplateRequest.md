# CreateWhatsAppTemplateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | 
**name** | **String** | Template name (lowercase, letters/numbers/underscores, must start with a letter) | 
**category** | **Category** | Template category (enum: AUTHENTICATION, MARKETING, UTILITY) | 
**language** | **String** | Template language code (e.g., en_US) | 
**components** | **Vec<serde_json::Value>** | Template components (header, body, footer, buttons) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


