# WhatsAppMessagePricing

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**billable** | Option<**bool**> | Whether Meta bills this message. Meta has announced it will deprecate this field. | 
**pricing_model** | Option<**String**> | `PMP` (per-message pricing) or `CBP` (conversation-based, messages before 2025-07-01). | 
**category** | Option<**String**> | Pricing category as Meta sends it, for example `marketing`, `marketing_lite`, `utility`, `authentication`, `authentication-international`, `service`, `referral_conversion`. | 
**r#type** | Option<**String**> | `regular` (billable), `free_customer_service` or `free_entry_point`. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


