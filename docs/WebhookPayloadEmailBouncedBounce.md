# WebhookPayloadEmailBouncedBounce

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**recipient** | Option<**String**> | The address that refused the mail. | [optional]
**r#type** | Option<**Type**> | `hard`: 5.x.x, the address does not take mail. `soft`: 4.x.x, a temporary refusal the sending server gave up on. `undetermined`: the report gave no status. (enum: hard, soft, undetermined) | [optional]
**category** | Option<**Category**> |  (enum: user_unknown, mailbox_full, domain_not_found, policy_blocked, spam_blocked, blocklisted, message_too_large, content_rejected, auth_failure, rate_limited, other) | [optional]
**status** | Option<**String**> | RFC 3463 enhanced status, such as 5.1.1. | [optional]
**smtp_code** | Option<**i32**> | The SMTP reply code, such as 550. Always a number. | [optional]
**diagnostic** | Option<**String**> | The receiving server's answer. | [optional]
**recommended_action** | Option<**RecommendedAction**> | `remove` only for an address that does not take mail. Sender-side refusals (authentication, blocklists, spam filters) are `fix_configuration` or `review`, never `remove`. (enum: remove, retry, review, fix_configuration) | [optional]
**reporting_mta** | Option<**String**> |  | [optional]
**detection** | Option<**Detection**> | `dsn`: a standard delivery report with the bounced Message-ID. `ndr`: a non-standard report read from its headers and text. (enum: dsn, ndr) | [optional]
**bounce_message_id** | Option<**String**> | Provider id of the bounce report in the mailbox. | [optional]
**bounced_at** | Option<**String**> | When the report arrived in the mailbox. | [optional]
**detected_at** | Option<**String**> | When Zernio read it. Reports can arrive minutes to days after the send. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


