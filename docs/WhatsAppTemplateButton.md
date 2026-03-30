# WhatsAppTemplateButton

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** |  (enum: quick_reply, url, phone_number, otp, flow, mpm, catalog) | 
**text** | **String** |  | 
**url** | Option<**String**> | Required when type is URL | [optional]
**example** | Option<**Vec<String>**> | Example values for URL suffix variables | [optional]
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


