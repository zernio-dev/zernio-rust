# OnRcsAgentStatusUpdatedRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**test** | Option<**bool**> | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional]
**id** | Option<**String**> | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. It identifies the event only, never an account or other resource. | [optional]
**event** | Option<**Event**> |  (enum: rcs.agent.status_updated) | [optional]
**timestamp** | Option<**String**> | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | [optional]
**agent** | Option<[**models::OnRcsAgentStatusUpdatedRequestAgent**](OnRcsAgentStatusUpdatedRequestAgent.md)> |  | [optional]
**status** | Option<**Status**> |  (enum: changes_requested, brand_vetting, agent_review, testing, launch_review, launching, live, rejected, deactivated) | [optional]
**reason** | Option<**String**> | Our review note on changes_requested, the reason on rejected, or why a launch filing bounced back to testing. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


