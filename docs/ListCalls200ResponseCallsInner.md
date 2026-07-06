# ListCalls200ResponseCallsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**_id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> | Owning social account. The unified /v1/calls/{id} detail + recording endpoints work for any channel; the channel-specific endpoints remain for account-scoped access. | [optional]
**conversation_id** | Option<**String**> | Inbox conversation with the counterparty, when one exists. | [optional]
**contact_id** | Option<**String**> | CRM Contact for the counterparty, when resolved. | [optional]
**channel** | Option<**Channel**> |  (enum: whatsapp, pstn) | [optional]
**direction** | Option<**Direction**> |  (enum: inbound, outbound) | [optional]
**from** | Option<**String**> | Caller number (E.164). | [optional]
**to** | Option<**String**> | Callee number (E.164). | [optional]
**forward_to** | Option<**String**> | Destination the call was routed to (tel:/sip:/wss:), snapshotted at routing time. | [optional]
**greeting** | Option<**String**> | Outbound PSTN only. Message spoken to the callee on answer, before the bridge. | [optional]
**status** | Option<**Status**> |  (enum: ringing, answered, ended, failed) | [optional]
**is_voicemail** | Option<**bool**> | True when an inbound call went to voicemail. | [optional]
**amd** | Option<**bool**> | Outbound answering-machine detection was requested for this call. | [optional]
**answered_machine** | Option<**bool**> | With `amd`, whether a machine (vs a human) answered. | [optional]
**forward_caller_id** | Option<**ForwardCallerId**> | Caller ID presented on the forwarded leg. (enum: business, caller) | [optional]
**recording_enabled** | Option<**bool**> | Effective flag for THIS call (number default + per-call override, resolved at create time). | [optional]
**transcription_enabled** | Option<**bool**> |  | [optional]
**transcription_language** | Option<**TranscriptionLanguage**> |  (enum: auto, en, es) | [optional]
**started_at** | Option<**String**> |  | [optional]
**answered_at** | Option<**String**> |  | [optional]
**ended_at** | Option<**String**> |  | [optional]
**transferred_at** | Option<**String**> | When the call was blind-transferred (POST /v1/voice/calls/{id}/transfer). | [optional]
**duration_seconds** | Option<**i32**> |  | [optional]
**end_reason** | Option<**EndReason**> |  (enum: hangup, no_answer, rejected, error) | [optional]
**hangup_cause** | Option<**String**> | Raw carrier hangup cause behind endReason (e.g. normal_clearing, not_found, time_limit) — the actual motive when endReason is a coarse bucket. | [optional]
**sip_hangup_cause** | Option<**String**> | SIP response code that ended the call, when SIP-signalled (e.g. '403', '488'). The real failure reason for SIP legs. | [optional]
**call_errors** | Option<[**Vec<models::CallRecordCallErrorsInner>**](CallRecordCallErrorsInner.md)> | Per-call failure log (dial failed, bridge failed, recording error). | [optional]
**recording_url** | Option<**String**> | May be expired. Resolve a fresh playable URL via GET /v1/calls/{id}/recording (any channel). | [optional]
**last_transcript_snippet** | Option<**String**> | Most recent transcript segment, for list previews. | [optional]
**transcript** | Option<[**Vec<models::CallRecordTranscriptInner>**](CallRecordTranscriptInner.md)> | Full transcript segments (detail endpoint only; omitted from lists). | [optional]
**billing** | Option<[**models::CallRecordBilling**](CallRecordBilling.md)> |  | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]
**contact_name** | Option<**String**> | CRM contact name for the counterparty, when resolved. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


