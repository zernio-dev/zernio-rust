# SendInboxMessageRequestInteractiveActionOneOf2Parameters

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**flow_message_version** | Option<**FlowMessageVersion**> | Defaults to \"3\" when omitted. (enum: 3) | [optional]
**flow_token** | **String** | Opaque token you choose to correlate Flow responses with your own state (max 200 chars). | 
**flow_id** | **String** | Published Flow ID from Meta Business Manager. | 
**flow_cta** | **String** | Button label that opens the Flow (max 20 chars). | 
**flow_action** | **FlowAction** | `navigate` sends the user to `flow_action_payload.screen`; `data_exchange` posts data to your Flow endpoint. (enum: navigate, data_exchange) | 
**flow_action_payload** | Option<[**models::SendInboxMessageRequestInteractiveActionOneOf2ParametersFlowActionPayload**](SendInboxMessageRequestInteractiveActionOneOf2ParametersFlowActionPayload.md)> |  | [optional]
**mode** | Option<**Mode**> | Set to `draft` to test an unpublished Flow. (enum: draft) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


