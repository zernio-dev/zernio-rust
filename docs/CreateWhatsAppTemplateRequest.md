# CreateWhatsAppTemplateRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | 
**name** | **String** | Template name (lowercase, letters/numbers/underscores, must start with a letter) | 
**category** | **Category** | Template category (enum: AUTHENTICATION, MARKETING, UTILITY) | 
**language** | **String** | Template language code (e.g., en_US) | 
**components** | Option<**Vec<serde_json::Value>**> | Template components (header, body, footer, buttons). Required for custom templates, omit when using library_template_name. | [optional]
**library_template_name** | Option<**String**> | Name of a pre-built template from Meta's template library (e.g., \"appointment_reminder\", \"auto_pay_reminder_1\", \"address_update\"). When provided, the template is pre-approved by Meta with no review wait. Omit `components` when using this field.  | [optional]
**library_template_body_inputs** | Option<**serde_json::Value**> | Optional body customizations for library templates. Available options depend on the template (e.g., add_contact_number, add_learn_more_link, add_security_recommendation, add_track_package_link, code_expiration_minutes).  | [optional]
**library_template_button_inputs** | Option<[**Vec<models::CreateWhatsAppTemplateRequestLibraryTemplateButtonInputsInner>**](CreateWhatsAppTemplateRequestLibraryTemplateButtonInputsInner.md)> | Optional button customizations for library templates. Each item specifies button type and configuration (e.g., URL, phone number, quick reply).  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


