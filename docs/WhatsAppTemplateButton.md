# WhatsAppTemplateButton

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** |  (enum: quick_reply, url, phone_number, otp, copy_code, flow, mpm, catalog) | 
**text** | Option<**String**> | Visible button label. Required for all types except copy_code (whose label is fixed by WhatsApp) and otp (omit it and WhatsApp supplies its own label, localized to the template language; an English label on a non-English template is rejected). | [optional]
**url** | Option<**String**> | Required when type is URL | [optional]
**example** | Option<**serde_json::Value**> |  | [optional]
**phone_number** | Option<**String**> | Required when type is phone_number | [optional]
**otp_type** | Option<**OtpType**> | Required when type is otp (enum: copy_code, one_tap, zero_tap) | [optional]
**autofill_text** | Option<**String**> |  | [optional]
**package_name** | Option<**String**> |  | [optional]
**signature_hash** | Option<**String**> |  | [optional]
**flow_id** | Option<**String**> |  | [optional]
**flow_name** | Option<**String**> |  | [optional]
**flow_json** | Option<**String**> |  | [optional]
**flow_action** | Option<**String**> |  | [optional]
**navigate_screen** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


