# WhatsAppTemplateButton

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** |  (enum: QUICK_REPLY, URL, PHONE_NUMBER, OTP, FLOW, MPM, CATALOG) | 
**text** | **String** |  | 
**url** | Option<**String**> | Required when type is URL | [optional]
**example** | Option<**Vec<String>**> | Example values for URL suffix variables | [optional]
**phone_number** | Option<**String**> | Required when type is PHONE_NUMBER | [optional]
**otp_type** | Option<**OtpType**> | Required when type is OTP (enum: COPY_CODE, ONE_TAP, ZERO_TAP) | [optional]
**autofill_text** | Option<**String**> |  | [optional]
**package_name** | Option<**String**> |  | [optional]
**signature_hash** | Option<**String**> |  | [optional]
**flow_id** | Option<**String**> |  | [optional]
**flow_name** | Option<**String**> |  | [optional]
**flow_json** | Option<**String**> |  | [optional]
**flow_action** | Option<**String**> |  | [optional]
**navigate_screen** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


