# SendInboxMessageRequestButtonsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** | Button type. phone is Facebook only. Ignored on WhatsApp (buttons always render as reply buttons). (enum: url, postback, phone) | 
**title** | **String** | Button label (max 20 chars) | 
**url** | Option<**String**> | URL for url-type buttons (Facebook/Instagram only) | [optional]
**payload** | Option<**String**> | Payload for postback-type buttons. On WhatsApp, this is the reply ID returned on the message.received webhook when the button is tapped. | [optional]
**phone** | Option<**String**> | Phone number for phone-type buttons (Facebook only) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


