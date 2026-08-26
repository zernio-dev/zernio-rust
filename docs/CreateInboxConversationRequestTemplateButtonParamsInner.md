# CreateInboxConversationRequestTemplateButtonParamsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**index** | **i32** | Zero-based position of the button in the approved template's buttons. | 
**sub_type** | **SubType** | The button kind, which decides how the value is sent: copy_code sends it as the coupon_code payload, flow as the flow token, url as the dynamic suffix appended to the button's base URL. (enum: url, copy_code, flow) | 
**value** | **String** | The value to send (e.g. the Pix copy-and-paste code for a copy_code button). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


