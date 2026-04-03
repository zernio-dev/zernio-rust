# SendWhatsAppFlowMessageRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | WhatsApp social account ID | 
**to** | **String** | Recipient phone number (E.164 format, e.g. +1234567890) | 
**flow_id** | **String** | Published flow ID | 
**flow_cta** | **String** | CTA button text (e.g. 'Book Now', 'Sign Up') | 
**flow_action** | Option<**FlowAction**> | Action type: navigate opens a screen directly, data_exchange hits your endpoint first (enum: navigate, data_exchange) | [optional][default to Navigate]
**flow_token** | Option<**String**> | Unique token to correlate responses. Auto-generated UUID if omitted. | [optional]
**flow_action_payload** | Option<[**models::SendWhatsAppFlowMessageRequestFlowActionPayload**](SendWhatsAppFlowMessageRequestFlowActionPayload.md)> |  | [optional]
**body** | **String** | Message body text | 
**header** | Option<[**models::SendWhatsAppFlowMessageRequestHeader**](SendWhatsAppFlowMessageRequestHeader.md)> |  | [optional]
**footer** | Option<**String**> | Optional footer text | [optional]
**draft** | Option<**bool**> | Set true to test an unpublished (DRAFT) flow | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


