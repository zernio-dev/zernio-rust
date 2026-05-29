# WhatsAppSandboxSession

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Session id. Use this to revoke via DELETE. | 
**phone_e164** | **String** | Digits-only E.164 form (no +, spaces, or dashes). | 
**status** | **Status** | `pending` until the phone replies to the activation template, then `active`. Expired sessions are pruned by TTL and never appear in list responses.  (enum: pending, active) | 
**expires_at** | **String** | UTC timestamp at which the session becomes invalid. Pending sessions get a 24h window; activated sessions get 7 days.  | 
**activated_at** | Option<**String**> | When the session transitioned `pending → active`, or null. | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


