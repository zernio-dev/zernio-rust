# CommentAutomationStats

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**triggered** | Option<**i32**> | Matched triggers that reached the audience or send stage. | [optional]
**dms_sent** | Option<**i32**> |  | [optional]
**dms_failed** | Option<**i32**> |  | [optional]
**unique_contacts** | Option<**i32**> |  | [optional]
**tracked_sends** | Option<**i32**> | DMs sent with a trackable (wrapped) link. CTR denominator: divide clicks by this, not dmsSent. Lags dmsSent for campaigns that predate click tracking. | [optional]
**link_clicks** | Option<**i32**> | Total clicks on tracked links (bots/prefetch excluded). | [optional]
**unique_clicks** | Option<**i32**> | Distinct people who clicked a tracked link. | [optional]
**delivered** | Option<**i32**> | DMs confirmed delivered (Messenger; IG emits no delivery receipt). | [optional]
**read** | Option<**i32**> | DMs confirmed read (IG messaging_seen / Messenger message_reads). | [optional]
**audience_skipped** | Option<**i32**> | Triggers the audience rule did not answer with the DM. | [optional]
**follow_gate_sent** | Option<**i32**> |  | [optional]
**follow_gate_passed** | Option<**i32**> |  | [optional]
**follow_gate_failed** | Option<**i32**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


