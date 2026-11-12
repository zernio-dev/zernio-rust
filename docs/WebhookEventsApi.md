# \WebhookEventsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**on_account_ads_initial_sync_completed**](WebhookEventsApi.md#on_account_ads_initial_sync_completed) | **POST** /account.ads.initial_sync_completed | Ads initial sync completed event
[**on_account_ads_sync_failed**](WebhookEventsApi.md#on_account_ads_sync_failed) | **POST** /account.ads.sync_failed | Ads sync failed event
[**on_account_ads_sync_recovered**](WebhookEventsApi.md#on_account_ads_sync_recovered) | **POST** /account.ads.sync_recovered | Ads sync recovered event
[**on_account_connected**](WebhookEventsApi.md#on_account_connected) | **POST** /account.connected | Account connected event
[**on_account_disconnected**](WebhookEventsApi.md#on_account_disconnected) | **POST** /account.disconnected | Account disconnected event
[**on_account_permissions_changed**](WebhookEventsApi.md#on_account_permissions_changed) | **POST** /account.permissions_changed | Account permissions changed event
[**on_account_rate_limited**](WebhookEventsApi.md#on_account_rate_limited) | **POST** /account.rate_limited | Mailbox sending cooldown started
[**on_ad_account_status_changed**](WebhookEventsApi.md#on_ad_account_status_changed) | **POST** /ad_account.status_changed | Ad account status changed event
[**on_ad_created**](WebhookEventsApi.md#on_ad_created) | **POST** /ad.created | Ad created event
[**on_ad_delivery_issue**](WebhookEventsApi.md#on_ad_delivery_issue) | **POST** /ad.delivery_issue | Ad delivery issue event
[**on_ad_review_approved**](WebhookEventsApi.md#on_ad_review_approved) | **POST** /ad.review.approved | Ad review approved event
[**on_ad_review_rejected**](WebhookEventsApi.md#on_ad_review_rejected) | **POST** /ad.review.rejected | Ad review rejected event
[**on_ad_rule_triggered**](WebhookEventsApi.md#on_ad_rule_triggered) | **POST** /ad_rule.triggered | Ad rule triggered event
[**on_ad_set_created**](WebhookEventsApi.md#on_ad_set_created) | **POST** /ad_set.created | Ad set created event
[**on_ad_set_updated**](WebhookEventsApi.md#on_ad_set_updated) | **POST** /ad_set.updated | Ad set updated event
[**on_ad_status_changed**](WebhookEventsApi.md#on_ad_status_changed) | **POST** /ad.status_changed | Ad status changed event
[**on_ad_updated**](WebhookEventsApi.md#on_ad_updated) | **POST** /ad.updated | Ad updated event
[**on_ad_video_processed**](WebhookEventsApi.md#on_ad_video_processed) | **POST** /ad.video.processed | Ad video processed event
[**on_analytics_synced**](WebhookEventsApi.md#on_analytics_synced) | **POST** /analytics.synced | Analytics synced event
[**on_api_changelog_published**](WebhookEventsApi.md#on_api_changelog_published) | **POST** /api.changelog.published | API changelog entry published event
[**on_automation_action_applied**](WebhookEventsApi.md#on_automation_action_applied) | **POST** /automation.action.applied | Automation action applied event
[**on_automation_action_failed**](WebhookEventsApi.md#on_automation_action_failed) | **POST** /automation.action.failed | Automation action failed event
[**on_automation_action_unknown**](WebhookEventsApi.md#on_automation_action_unknown) | **POST** /automation.action.unknown | Automation action unknown event
[**on_automation_alert_escalated**](WebhookEventsApi.md#on_automation_alert_escalated) | **POST** /automation.alert.escalated | Automation alert escalated event
[**on_automation_alert_opened**](WebhookEventsApi.md#on_automation_alert_opened) | **POST** /automation.alert.opened | Automation alert opened event
[**on_automation_alert_resolved**](WebhookEventsApi.md#on_automation_alert_resolved) | **POST** /automation.alert.resolved | Automation alert resolved event
[**on_automation_check_completed**](WebhookEventsApi.md#on_automation_check_completed) | **POST** /automation.check.completed | Automation check completed event
[**on_balance_charged**](WebhookEventsApi.md#on_balance_charged) | **POST** /balance.charged | Balance charged event
[**on_balance_empty**](WebhookEventsApi.md#on_balance_empty) | **POST** /balance.empty | Balance empty event
[**on_balance_low**](WebhookEventsApi.md#on_balance_low) | **POST** /balance.low | Balance low event
[**on_branded_calling_identity_action_required**](WebhookEventsApi.md#on_branded_calling_identity_action_required) | **POST** /branded_calling.identity.action_required | Caller identity action required event
[**on_branded_calling_identity_status_updated**](WebhookEventsApi.md#on_branded_calling_identity_status_updated) | **POST** /branded_calling.identity.status_updated | Caller identity status updated event
[**on_branded_calling_number_status_updated**](WebhookEventsApi.md#on_branded_calling_number_status_updated) | **POST** /branded_calling.number.status_updated | Branded number status updated event
[**on_calendar_event_created**](WebhookEventsApi.md#on_calendar_event_created) | **POST** /calendar.event.created | Calendar event created
[**on_calendar_event_deleted**](WebhookEventsApi.md#on_calendar_event_deleted) | **POST** /calendar.event.deleted | Calendar event deleted
[**on_calendar_event_updated**](WebhookEventsApi.md#on_calendar_event_updated) | **POST** /calendar.event.updated | Calendar event updated
[**on_call_ended**](WebhookEventsApi.md#on_call_ended) | **POST** /call.ended | Call ended event
[**on_call_failed**](WebhookEventsApi.md#on_call_failed) | **POST** /call.failed | Call failed event
[**on_call_permission_request**](WebhookEventsApi.md#on_call_permission_request) | **POST** /call.permission_request | Call permission request reply event
[**on_call_received**](WebhookEventsApi.md#on_call_received) | **POST** /call.received | Call received event
[**on_call_recording_ready**](WebhookEventsApi.md#on_call_recording_ready) | **POST** /call.recording_ready | Call recording ready event
[**on_call_transcript_segment**](WebhookEventsApi.md#on_call_transcript_segment) | **POST** /call.transcript_segment | Call transcript segment event
[**on_campaign_budget_depleted**](WebhookEventsApi.md#on_campaign_budget_depleted) | **POST** /campaign.budget.depleted | Campaign budget depleted event
[**on_campaign_created**](WebhookEventsApi.md#on_campaign_created) | **POST** /campaign.created | Campaign created event
[**on_campaign_draft_approved**](WebhookEventsApi.md#on_campaign_draft_approved) | **POST** /campaign_draft.approved | Campaign draft approved event
[**on_campaign_draft_rejected**](WebhookEventsApi.md#on_campaign_draft_rejected) | **POST** /campaign_draft.rejected | Campaign draft rejected event
[**on_campaign_draft_revision_requested**](WebhookEventsApi.md#on_campaign_draft_revision_requested) | **POST** /campaign_draft.revision_requested | Campaign draft revision requested event
[**on_campaign_draft_submitted**](WebhookEventsApi.md#on_campaign_draft_submitted) | **POST** /campaign_draft.submitted | Campaign draft submitted event
[**on_campaign_participant_approved**](WebhookEventsApi.md#on_campaign_participant_approved) | **POST** /campaign_participant.approved | Campaign participant approved event
[**on_campaign_participant_denied**](WebhookEventsApi.md#on_campaign_participant_denied) | **POST** /campaign_participant.denied | Campaign participant denied event
[**on_campaign_participant_joined**](WebhookEventsApi.md#on_campaign_participant_joined) | **POST** /campaign_participant.joined | Campaign participant joined event
[**on_campaign_participant_pending**](WebhookEventsApi.md#on_campaign_participant_pending) | **POST** /campaign_participant.pending | Campaign participant pending event
[**on_campaign_participant_removed**](WebhookEventsApi.md#on_campaign_participant_removed) | **POST** /campaign_participant.removed | Campaign participant removed event
[**on_campaign_participant_suspended**](WebhookEventsApi.md#on_campaign_participant_suspended) | **POST** /campaign_participant.suspended | Campaign participant suspended event
[**on_campaign_payout_failed**](WebhookEventsApi.md#on_campaign_payout_failed) | **POST** /campaign_payout.failed | Campaign payout failed event
[**on_campaign_payout_payable**](WebhookEventsApi.md#on_campaign_payout_payable) | **POST** /campaign_payout.payable | Campaign payout payable event
[**on_campaign_payout_settled**](WebhookEventsApi.md#on_campaign_payout_settled) | **POST** /campaign_payout.settled | Campaign payout settled event
[**on_campaign_sample_approved**](WebhookEventsApi.md#on_campaign_sample_approved) | **POST** /campaign_sample.approved | Campaign sample approved event
[**on_campaign_sample_declined**](WebhookEventsApi.md#on_campaign_sample_declined) | **POST** /campaign_sample.declined | Campaign sample declined event
[**on_campaign_sample_requested**](WebhookEventsApi.md#on_campaign_sample_requested) | **POST** /campaign_sample.requested | Campaign sample requested event
[**on_campaign_sample_shipped**](WebhookEventsApi.md#on_campaign_sample_shipped) | **POST** /campaign_sample.shipped | Campaign sample shipped event
[**on_campaign_submission_approved**](WebhookEventsApi.md#on_campaign_submission_approved) | **POST** /campaign_submission.approved | Campaign submission approved event
[**on_campaign_submission_flagged**](WebhookEventsApi.md#on_campaign_submission_flagged) | **POST** /campaign_submission.flagged | Campaign submission flagged event
[**on_campaign_submission_pending_review**](WebhookEventsApi.md#on_campaign_submission_pending_review) | **POST** /campaign_submission.pending_review | Campaign submission pending review event
[**on_campaign_submission_received**](WebhookEventsApi.md#on_campaign_submission_received) | **POST** /campaign_submission.received | Campaign submission received event
[**on_campaign_submission_rejected**](WebhookEventsApi.md#on_campaign_submission_rejected) | **POST** /campaign_submission.rejected | Campaign submission rejected event
[**on_campaign_updated**](WebhookEventsApi.md#on_campaign_updated) | **POST** /campaign.updated | Campaign updated event
[**on_comment_received**](WebhookEventsApi.md#on_comment_received) | **POST** /comment.received | Comment received event
[**on_commerce_order_created**](WebhookEventsApi.md#on_commerce_order_created) | **POST** /commerce.order.created | Commerce order created event
[**on_commerce_order_refunded**](WebhookEventsApi.md#on_commerce_order_refunded) | **POST** /commerce.order.refunded | Commerce order refunded event
[**on_commerce_order_updated**](WebhookEventsApi.md#on_commerce_order_updated) | **POST** /commerce.order.updated | Commerce order updated event
[**on_commerce_product_created**](WebhookEventsApi.md#on_commerce_product_created) | **POST** /commerce.product.created | Commerce product created event
[**on_commerce_product_deleted**](WebhookEventsApi.md#on_commerce_product_deleted) | **POST** /commerce.product.deleted | Commerce product deleted event
[**on_commerce_product_updated**](WebhookEventsApi.md#on_commerce_product_updated) | **POST** /commerce.product.updated | Commerce product updated event
[**on_contact_deleted**](WebhookEventsApi.md#on_contact_deleted) | **POST** /contact.deleted | Contact deleted
[**on_contact_field_changed**](WebhookEventsApi.md#on_contact_field_changed) | **POST** /contact.field_changed | Contact field changed event
[**on_contact_tag_added**](WebhookEventsApi.md#on_contact_tag_added) | **POST** /contact.tag_added | Contact tag added event
[**on_contact_tag_removed**](WebhookEventsApi.md#on_contact_tag_removed) | **POST** /contact.tag_removed | Contact tag removed event
[**on_contact_updated**](WebhookEventsApi.md#on_contact_updated) | **POST** /contact.updated | Contact updated
[**on_conversation_control_changed**](WebhookEventsApi.md#on_conversation_control_changed) | **POST** /conversation.control_changed | Conversation control changed event
[**on_conversation_started**](WebhookEventsApi.md#on_conversation_started) | **POST** /conversation.started | Conversation started event
[**on_conversion_received**](WebhookEventsApi.md#on_conversion_received) | **POST** /conversion.received | Conversion received event
[**on_creator_campaign_budget_exhausted**](WebhookEventsApi.md#on_creator_campaign_budget_exhausted) | **POST** /creator_campaign.budget_exhausted | Creator campaign budget exhausted event
[**on_creator_campaign_closed**](WebhookEventsApi.md#on_creator_campaign_closed) | **POST** /creator_campaign.closed | Creator campaign closed event
[**on_email_bounced**](WebhookEventsApi.md#on_email_bounced) | **POST** /email.bounced | Email bounced
[**on_email_deleted**](WebhookEventsApi.md#on_email_deleted) | **POST** /email.deleted | Email deleted
[**on_email_link_clicked**](WebhookEventsApi.md#on_email_link_clicked) | **POST** /email.link_clicked | Email link clicked
[**on_email_opened**](WebhookEventsApi.md#on_email_opened) | **POST** /email.opened | Email opened
[**on_email_send_failed**](WebhookEventsApi.md#on_email_send_failed) | **POST** /email.send_failed | Scheduled email failed
[**on_email_sent**](WebhookEventsApi.md#on_email_sent) | **POST** /email.sent | Email sent
[**on_email_thread_replied**](WebhookEventsApi.md#on_email_thread_replied) | **POST** /email.thread_replied | Email thread replied
[**on_email_updated**](WebhookEventsApi.md#on_email_updated) | **POST** /email.updated | Email updated
[**on_file_created**](WebhookEventsApi.md#on_file_created) | **POST** /file.created | File created
[**on_file_deleted**](WebhookEventsApi.md#on_file_deleted) | **POST** /file.deleted | File deleted
[**on_file_picked**](WebhookEventsApi.md#on_file_picked) | **POST** /file.picked | Files picked
[**on_file_updated**](WebhookEventsApi.md#on_file_updated) | **POST** /file.updated | File updated
[**on_lead_received**](WebhookEventsApi.md#on_lead_received) | **POST** /lead.received | Lead received event
[**on_mention_received**](WebhookEventsApi.md#on_mention_received) | **POST** /mention.received | Mention received event
[**on_message_deleted**](WebhookEventsApi.md#on_message_deleted) | **POST** /message.deleted | Message deleted event
[**on_message_delivered**](WebhookEventsApi.md#on_message_delivered) | **POST** /message.delivered | Message delivered event
[**on_message_edited**](WebhookEventsApi.md#on_message_edited) | **POST** /message.edited | Message edited event
[**on_message_failed**](WebhookEventsApi.md#on_message_failed) | **POST** /message.failed | Message delivery failed event
[**on_message_played**](WebhookEventsApi.md#on_message_played) | **POST** /message.played | Message played event
[**on_message_read**](WebhookEventsApi.md#on_message_read) | **POST** /message.read | Message read event
[**on_message_received**](WebhookEventsApi.md#on_message_received) | **POST** /message.received | Message received event
[**on_message_sent**](WebhookEventsApi.md#on_message_sent) | **POST** /message.sent | Message sent event
[**on_notification_sent**](WebhookEventsApi.md#on_notification_sent) | **POST** /notification.sent | Notification sent event
[**on_phone_number_stock_available**](WebhookEventsApi.md#on_phone_number_stock_available) | **POST** /phone_number.stock_available | Phone-number stock available event
[**on_post_authenticity_changed**](WebhookEventsApi.md#on_post_authenticity_changed) | **POST** /post.authenticity_changed | Post authenticity changed event
[**on_post_cancelled**](WebhookEventsApi.md#on_post_cancelled) | **POST** /post.cancelled | Post cancelled event
[**on_post_external_created**](WebhookEventsApi.md#on_post_external_created) | **POST** /post.external.created | External post created event
[**on_post_external_deleted**](WebhookEventsApi.md#on_post_external_deleted) | **POST** /post.external.deleted | External post deleted event
[**on_post_external_updated**](WebhookEventsApi.md#on_post_external_updated) | **POST** /post.external.updated | External post updated event
[**on_post_failed**](WebhookEventsApi.md#on_post_failed) | **POST** /post.failed | Post failed event
[**on_post_partial**](WebhookEventsApi.md#on_post_partial) | **POST** /post.partial | Post partial event
[**on_post_platform_deleted**](WebhookEventsApi.md#on_post_platform_deleted) | **POST** /post.platform.deleted | Post platform deleted event
[**on_post_platform_failed**](WebhookEventsApi.md#on_post_platform_failed) | **POST** /post.platform.failed | Post platform failed event
[**on_post_platform_published**](WebhookEventsApi.md#on_post_platform_published) | **POST** /post.platform.published | Post platform published event
[**on_post_published**](WebhookEventsApi.md#on_post_published) | **POST** /post.published | Post published event
[**on_post_recycled**](WebhookEventsApi.md#on_post_recycled) | **POST** /post.recycled | Post recycled event
[**on_post_scheduled**](WebhookEventsApi.md#on_post_scheduled) | **POST** /post.scheduled | Post scheduled event
[**on_post_tik_tok_url_resolved**](WebhookEventsApi.md#on_post_tik_tok_url_resolved) | **POST** /post.tiktok.url_resolved | TikTok post URL resolved event
[**on_post_tracking_completed**](WebhookEventsApi.md#on_post_tracking_completed) | **POST** /post.tracking_completed | Post tracking completed event
[**on_rcs_agent_status_updated**](WebhookEventsApi.md#on_rcs_agent_status_updated) | **POST** /rcs.agent.status_updated | RCS agent status updated event
[**on_reaction_received**](WebhookEventsApi.md#on_reaction_received) | **POST** /reaction.received | Reaction received event
[**on_referral_received**](WebhookEventsApi.md#on_referral_received) | **POST** /referral.received | Referral received event
[**on_review_deleted**](WebhookEventsApi.md#on_review_deleted) | **POST** /review.deleted | Review deleted event
[**on_review_new**](WebhookEventsApi.md#on_review_new) | **POST** /review.new | Review new event
[**on_review_restored**](WebhookEventsApi.md#on_review_restored) | **POST** /review.restored | Review restored event
[**on_review_updated**](WebhookEventsApi.md#on_review_updated) | **POST** /review.updated | Review updated event
[**on_sequence_enrolled**](WebhookEventsApi.md#on_sequence_enrolled) | **POST** /sequence.enrolled | Sequence enrolled event
[**on_sequence_exited**](WebhookEventsApi.md#on_sequence_exited) | **POST** /sequence.exited | Sequence exited event
[**on_sms_registration_action_required**](WebhookEventsApi.md#on_sms_registration_action_required) | **POST** /sms.registration.action_required | SMS registration action required event
[**on_sms_registration_status_updated**](WebhookEventsApi.md#on_sms_registration_status_updated) | **POST** /sms.registration.status_updated | SMS registration status updated event
[**on_support_run_completed**](WebhookEventsApi.md#on_support_run_completed) | **POST** /support.run.completed | Support Assistant finished event
[**on_support_run_failed**](WebhookEventsApi.md#on_support_run_failed) | **POST** /support.run.failed | Support Assistant failed event
[**on_verification_approved**](WebhookEventsApi.md#on_verification_approved) | **POST** /verification.approved | Verification approved event
[**on_verification_failed**](WebhookEventsApi.md#on_verification_failed) | **POST** /verification.failed | Verification failed event
[**on_webhook_test**](WebhookEventsApi.md#on_webhook_test) | **POST** /webhook.test | Webhook test event
[**on_whats_app_account_alert_received**](WebhookEventsApi.md#on_whats_app_account_alert_received) | **POST** /whatsapp.account.alert_received | WhatsApp account alert received
[**on_whats_app_account_name_status_updated**](WebhookEventsApi.md#on_whats_app_account_name_status_updated) | **POST** /whatsapp.account.name_status_updated | WhatsApp display-name review outcome event
[**on_whats_app_account_quality_updated**](WebhookEventsApi.md#on_whats_app_account_quality_updated) | **POST** /whatsapp.account.quality_updated | WhatsApp quality rating or messaging limit changed
[**on_whats_app_account_status_updated**](WebhookEventsApi.md#on_whats_app_account_status_updated) | **POST** /whatsapp.account.status_updated | WhatsApp Business Account restricted or reinstated
[**on_whats_app_automatic_event**](WebhookEventsApi.md#on_whats_app_automatic_event) | **POST** /whatsapp.automatic_event | WhatsApp automatic event detected
[**on_whats_app_contact_identity_changed**](WebhookEventsApi.md#on_whats_app_contact_identity_changed) | **POST** /whatsapp.contact.identity_changed | WhatsApp contact identity changed event
[**on_whats_app_number_action_required**](WebhookEventsApi.md#on_whats_app_number_action_required) | **POST** /whatsapp.number.action_required | WhatsApp number action required event
[**on_whats_app_number_activated**](WebhookEventsApi.md#on_whats_app_number_activated) | **POST** /whatsapp.number.activated | WhatsApp number activated event
[**on_whats_app_number_declined**](WebhookEventsApi.md#on_whats_app_number_declined) | **POST** /whatsapp.number.declined | WhatsApp number declined event
[**on_whats_app_number_kyc_submitted**](WebhookEventsApi.md#on_whats_app_number_kyc_submitted) | **POST** /whatsapp.number.kyc_submitted | WhatsApp number KYC submitted event
[**on_whats_app_number_reactivated**](WebhookEventsApi.md#on_whats_app_number_reactivated) | **POST** /whatsapp.number.reactivated | WhatsApp number reactivated event
[**on_whats_app_number_released**](WebhookEventsApi.md#on_whats_app_number_released) | **POST** /whatsapp.number.released | WhatsApp number released event
[**on_whats_app_number_suspended**](WebhookEventsApi.md#on_whats_app_number_suspended) | **POST** /whatsapp.number.suspended | WhatsApp number suspended event
[**on_whats_app_number_verification_required**](WebhookEventsApi.md#on_whats_app_number_verification_required) | **POST** /whatsapp.number.verification_required | WhatsApp number verification-required event
[**on_whats_app_template_category_updated**](WebhookEventsApi.md#on_whats_app_template_category_updated) | **POST** /whatsapp.template.category_updated | WhatsApp template category updated event
[**on_whats_app_template_status_updated**](WebhookEventsApi.md#on_whats_app_template_status_updated) | **POST** /whatsapp.template.status_updated | WhatsApp template status updated event
[**on_workflow_run_completed**](WebhookEventsApi.md#on_workflow_run_completed) | **POST** /workflow.run.completed | Workflow run completed event
[**on_workflow_run_failed**](WebhookEventsApi.md#on_workflow_run_failed) | **POST** /workflow.run.failed | Workflow run failed event
[**on_workflow_run_started**](WebhookEventsApi.md#on_workflow_run_started) | **POST** /workflow.run.started | Workflow run started event



## on_account_ads_initial_sync_completed

> on_account_ads_initial_sync_completed(webhook_payload_account_ads_initial_sync_completed)
Ads initial sync completed event

The initial sync, ad-account discovery plus a 90-day ad backfill, completed for an ads-enabled account.  ### When it fires  Fires once per ads-enabled account. `sync` reports whether the backfill succeeded fully or partially, and how many ads were synced versus failed.  ### Scoped connects  When scoping was applied at connect time, `account.platformAdAccountId` echoes the chosen ad account when the scope is exactly one. `account.platformAdAccountIds` lists every `act_*` synced.  ### On failure  When `sync.status` is `\"failure\"`, the payload adds `sync.error` (raw platform error, about 2 KB), `sync.errorCode` and `sync.errorSubcode` when parseable, and `sync.errorCategory`.  ### Error categories  `sync.errorCategory` is `token_invalid`, `permission_denied`, `no_ad_accounts`, `rate_limited`, `discovery_failed` or `unknown`. New values may be added; existing ones are stable.  ### Retrying  Reconnecting re-queues the backfill and the event fires again. It fixes `token_invalid`, `permission_denied` and `rate_limited`; `no_ad_accounts` needs an ad account on the grant first.  ### When a retry is skipped  Zernio skips the re-queue only when a backfill already completed with at least one ad, or one started less than 20 minutes ago. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_account_ads_initial_sync_completed** | [**WebhookPayloadAccountAdsInitialSyncCompleted**](WebhookPayloadAccountAdsInitialSyncCompleted.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_account_ads_sync_failed

> on_account_ads_sync_failed(webhook_payload_account_ads_sync_failed)
Ads sync failed event

An ad account's ads stopped syncing: no success for 24 hours, or every live ad at the retry cap.  ### When it fires  An hourly check covers every ad account with live ads on a connected account, on any ads platform. Fires once per ad account until `account.ads.sync_recovered`.  ### Stale metrics  Metrics for the ad account are stale in between. Use this signal to flag the numbers in your UI rather than to poll.  ### Payload notes  `adAccount.platformAdAccountId` names the ad account (`act_*` on Meta). `account.accountId` names its connection, so one connection with several ad accounts reports each separately.  ### Sync fields  `sync.lastSuccessfulSyncAt` is the last good sync and `sync.failureCount` the consecutive failed attempts.  ### Error categories  Branch on `sync.errorCategory`: `ad_account_not_listed` (access removed or platform change; check permissions, reconnect), `sync_error` (see `sync.error`) or `stale` (no error recorded; retries usually clear it). New values may be added.  ### When it does not fire  A disconnected connection gets `account.disconnected` instead, and no recovery event follows. An ad account that never synced successfully, or whose last good sync is over 3 days old, is not announced. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_account_ads_sync_failed** | [**WebhookPayloadAccountAdsSyncFailed**](WebhookPayloadAccountAdsSyncFailed.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_account_ads_sync_recovered

> on_account_ads_sync_recovered(webhook_payload_account_ads_sync_recovered)
Ads sync recovered event

An ad account previously reported by `account.ads.sync_failed` synced successfully again.  ### When it fires  Fires once when a sync succeeds again, found by an hourly check.  ### Payload notes  `sync.failingSince` is the last successful sync before the failure started. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_account_ads_sync_recovered** | [**WebhookPayloadAccountAdsSyncRecovered**](WebhookPayloadAccountAdsSyncRecovered.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_account_connected

> on_account_connected(webhook_payload_account_connected)
Account connected event

An account was connected to a profile, through OAuth or credentials.  ### Repeat events  Reconnecting an account you already hold fires it again with the same `accountId`, since the connect flow upserts per profile and platform. Key your upsert on `accountId`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_account_connected** | [**WebhookPayloadAccountConnected**](WebhookPayloadAccountConnected.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_account_disconnected

> on_account_disconnected(webhook_payload_account_disconnected)
Account disconnected event

A connected account stopped working or was removed.  ### Intentional  Removed on purpose, such as `DELETE /v1/accounts/{id}` or a switch to the Free plan. Kept 1 hour (`gracePeriodEndsAt`), then deleted with no further event. Reconnecting within the hour restores the same `accountId`.  ### Unintentional  The connection broke (token expired or revoked, access lost). The account stays inactive until reconnected, keeping its `accountId`. Removing it instead sends a second event with `intentional`.  ### Immediate paths  An API removal emits at once with `disconnectionType: \"intentional\"`. A phone-side WhatsApp disconnect emits within seconds of Meta's notification, with `unintentional`.  ### WhatsApp reason  `reason` carries Meta's explanation. Deliberate: `BUSINESS_DOWNGRADE`, `CHANGE_NUMBER`, `USER_RE_REGISTERED`. Idle number dropped by Meta: `PRIMARY_INACTIVITY` after about 14 days, `COMPANION_INACTIVITY` after about 30.  ### Expired or revoked grants  A publish or analytics sync getting a definitive auth error deactivates the account. Publish tries a token refresh first, so the event means the refresh failed too. `reason` carries the platform's message.  ### Reconnection flags  A dead token on an ads or blog call flags the account, and the posting account sharing its token (`needsReconnection: true`). Each flagged account emits once; a later deactivation emits again, then not until reconnected.  ### Lead forms while disconnected  While a Facebook Page is flagged or deactivated, `GET /v1/ads/lead-forms/{formId}/leads` answers `409` with `code: \"account_disconnected\"`.  ### Reconciliation  Anything else (a number deleted in WhatsApp Manager, a channel Meta silently stops serving) is caught by periodic reconciliation, not a notification. It lags minutes to about a day.  ### Do not rely on its absence  Meta's notifications are best-effort. For WhatsApp, poll `GET /v1/whatsapp/number-info` or account health, which runs a live Meta link probe.  ### Subscribing  A webhook only receives the events it lists, so add `account.disconnected` explicitly. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_account_disconnected** | [**WebhookPayloadAccountDisconnected**](WebhookPayloadAccountDisconnected.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_account_permissions_changed

> on_account_permissions_changed(webhook_payload_account_permissions_changed)
Account permissions changed event

A publish on an account connected through your own OAuth app failed for a missing permission.  ### Behaviour  The account stays connected and its token still works. `account.missingScopeAreas` accumulates the affected areas, today `posting`. Each area sends one event, however many posts fail afterwards.  ### When it does not fire  Accounts not connected through your own OAuth app. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_account_permissions_changed** | [**WebhookPayloadAccountPermissionsChanged**](WebhookPayloadAccountPermissionsChanged.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_account_rate_limited

> on_account_rate_limited(webhook_payload_account_rate_limited)
Mailbox sending cooldown started

A Google or Microsoft mailbox was paused after sending one body to over 50 recipients in an hour.  ### Payload notes  `account.reason` says why and `account.resetsAt` says when sending resumes. Sends answer 429 until then. A later trigger can also start a cooldown. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_account_rate_limited** | [**WebhookPayloadAccountRateLimited**](WebhookPayloadAccountRateLimited.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_ad_account_status_changed

> on_ad_account_status_changed(webhook_payload_ad_account_status_changed)
Ad account status changed event

An ad account Zernio already tracked became `active`, `restricted`, `disabled` or `closed`.  ### When it fires  Fires when ad account discovery sees a tracked ad account change status, at most once per account per 24 hours. Covers Meta, Google, TikTok and X.  ### Status values  `restricted` needs something settled first (unpaid Meta balance, risk review, TikTok limit or pending verification, X review). `disabled` means the platform disabled or rejected it; `closed` means closed or pending closure.  ### Payload notes  `status.current` and `status.previous` use one vocabulary on every network. `status.raw` is the platform's own value, for example Meta's `account_status` code `2`.  ### When it does not fire  An account seen for the first time, an account Zernio has not seen in the last 48 hours, or a platform status Zernio does not recognize. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_ad_account_status_changed** | [**WebhookPayloadAdAccountStatusChanged**](WebhookPayloadAdAccountStatusChanged.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_ad_created

> on_ad_created(webhook_payload_ad_created)
Ad created event

An ad was created through Zernio (`source: \"zernio\"`) or detected by the sync (`source: \"platform\"`).  ### When it fires  Fires once the ad's campaign and ad set are recorded. A detected ad arrives up to one sync interval late; Meta ads entering review usually arrive within minutes.  ### When it does not fire  History loaded when an account connects, and ads created more than 7 days ago, are never announced. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_ad_created** | [**WebhookPayloadAdCreated**](WebhookPayloadAdCreated.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_ad_delivery_issue

> on_ad_delivery_issue(webhook_payload_ad_delivery_issue)
Ad delivery issue event

An ad Zernio already tracked moved into the platform's error state and stopped delivering.  ### What triggers it  Meta `WITH_ISSUES` (payment, policy or account problems), TikTok account punishment or missing balance, or any platform status Zernio does not recognize yet (check `issue.raw`).  ### When it fires  Fires at most once per ad per 24 hours. Ads seen for the first time by a sync never fire it.  ### Payload notes  `issue.raw` is the platform's status string. On Meta, `issue.reasons` carries Meta's messages for the campaign; other networks send none, so it is empty.  ### Platform notes  On Meta the same problem can also arrive as `ad.status_changed` with `WITH_ISSUES`, straight from Meta's webhook and usually sooner. Pick one of the two to act on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_ad_delivery_issue** | [**WebhookPayloadAdDeliveryIssue**](WebhookPayloadAdDeliveryIssue.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_ad_review_approved

> on_ad_review_approved(webhook_payload_ad_review)
Ad review approved event

An ad Zernio already tracked passed platform review, or a rejected ad was approved on appeal.  ### When it fires  Fires within one sync cycle of the platform's decision, not instantly; on Meta the review poll usually reports sooner. Each outcome is delivered at most once per ad per 24 hours.  ### When it does not fire  Ads seen for the first time by a sync never fire it, including history loaded at connect. On Meta, Google, TikTok and Reddit an ad that leaves review while paused sends no `approved`.  ### Platform notes  Covers every ad network Zernio syncs, with one payload shape. On X, Pinterest and LinkedIn the review is read apart from delivery status, so an ad leaving review while paused still sends `approved`.  ### Payload notes  `review.raw` is the platform's own status string. `adObject.adId` is the Zernio ad id, ready for `GET /v1/ads/{adId}`. Deduplicate on the event `id`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_ad_review** | [**WebhookPayloadAdReview**](WebhookPayloadAdReview.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_ad_review_rejected

> on_ad_review_rejected(webhook_payload_ad_review)
Ad review rejected event

The platform rejected an ad Zernio already tracked; `review.reasons` carries its reason when it gives one.  ### When it fires  Fires within one sync cycle of the platform's decision, not instantly; on Meta the review poll usually reports sooner. Each outcome is delivered at most once per ad per 24 hours.  ### When it does not fire  Ads seen for the first time by a sync never fire it, including history loaded at connect.  ### Platform notes  Covers every ad network Zernio syncs. Pinterest, LinkedIn and Reddit send their own reasons, X sends none, and most other networks return a generic message.  ### Payload notes  `review.raw` is the platform's own status string. Show `review.reasons` rather than branching on it. `adObject.adId` is the Zernio ad id. Deduplicate on the event `id`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_ad_review** | [**WebhookPayloadAdReview**](WebhookPayloadAdReview.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_ad_rule_triggered

> on_ad_rule_triggered(webhook_payload_ad_rule_triggered)
Ad rule triggered event

A scheduled run of an ad rule with a `notify` action found campaigns or ad sets meeting every condition.  ### When it fires  Each object is announced at most once per rule cooldown. A run where every object is still in cooldown sends nothing.  ### Failed actions  An object whose action `failed` gets no cooldown, so the next run retries it and reports it again.  ### Payload notes  `objects` lists only the objects the run acted on. `objects[].conditions` repeats every condition of the rule with `actual`, the value the object reached.  ### Actions  `objects[].actions` says what the rule did: `done`, `skipped` (with a `reason` such as `already_paused` or `at_limit`) or `failed`. On `adjust_budget` it carries `previousDailyBudget` and `newDailyBudget`; empty on a notify-only rule.  ### Run context  `run.today` and `run.timezone` give the ad account's calendar date the windows used. `run.timezoneAssumed` is `true` when UTC was assumed. `run.currency` is the currency of money metrics, or `null` when unknown. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_ad_rule_triggered** | [**WebhookPayloadAdRuleTriggered**](WebhookPayloadAdRuleTriggered.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_ad_set_created

> on_ad_set_created(webhook_payload_ad_set_created)
Ad set created event

An ad set was created through Zernio (`source: \"zernio\"`) or detected by the sync (`source: \"platform\"`).  ### When it fires  Fires once the ad set row is recorded, so `GET /v1/ads/ad-sets/{adSetId}` finds it. A detected ad set arrives up to one sync interval late.  ### Payload notes  `adObject.campaign` is the campaign the ad set belongs to, or null when the platform has none.  ### When it does not fire  History loaded when an account connects, and ad sets created more than 7 days ago, are never announced. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_ad_set_created** | [**WebhookPayloadAdSetCreated**](WebhookPayloadAdSetCreated.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_ad_set_updated

> on_ad_set_updated(webhook_payload_ad_set_updated)
Ad set updated event

An ad set was edited through Zernio (`source: \"zernio\"`), or outside Zernio and detected by the sync (`source: \"platform\"`).  ### When it fires  Fires after the platform and Zernio both accepted the edit. Outside edits arrive up to one sync interval late, and only to the user whose sync saw them.  ### Deduplication  Events are not deduplicated, so every edit is announced. Use the event `id` to drop repeats.  ### Payload notes  `changes` lists the edited fields: `name`, `status` (the ad set's own on/off switch), `budget`, `bid`, `schedule`, `targeting` or `settings`. Ignore unknown values. It never carries old or new values, so read the ad set.  ### What the sync detects  From the sync, `changes` covers only `name` and `status`. Status is not detected on Reddit.  ### When it does not fire  History loaded when an account connects is never announced. Budget and targeting edits made through `PUT /v1/ads/{adId}` arrive as `ad.updated`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_ad_set_updated** | [**WebhookPayloadAdSetUpdated**](WebhookPayloadAdSetUpdated.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_ad_status_changed

> on_ad_status_changed(webhook_payload_ad_status_changed)
Ad status changed event

A campaign, ad set or ad on a connected Meta ad account (`metaads`) changed status.  ### Sources  Two Meta `ad_account` fields feed it: `in_process_ad_objects` (finished processing, `status.raw` is Meta's `status_name`) and `with_issues_ad_objects` (`status.raw` is `WITH_ISSUES`, `error` filled from Meta).  ### Payload notes  `adObject.level` is `CAMPAIGN`, `AD_SET` or `AD`; creative-level events are not forwarded. Branch on `status.raw`. Use `error.code` as the stable discriminator, since `error.summary` and `error.message` are localized to the owner's Meta locale.  ### The error block  `error` is present on most `WITH_ISSUES` events but can be absent, and never appears on any other status. Null-check it before reading `error.code`.  ### Fan-out  Matching is keyed on `adObject.platformAdAccountId`. When several connected `metaads` accounts point at the same Meta ad account, each receives its own delivery. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_ad_status_changed** | [**WebhookPayloadAdStatusChanged**](WebhookPayloadAdStatusChanged.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_ad_updated

> on_ad_updated(webhook_payload_ad_updated)
Ad updated event

An ad was edited through Zernio (`source: \"zernio\"`), or outside Zernio and detected by the sync (`source: \"platform\"`).  ### When it fires  Fires once, to the owner of the edited ad. Outside edits arrive up to one sync interval late. Every edit is announced, so use the event `id` to drop repeats.  ### Payload notes  `changes` lists the edited fields: `name`, `status` (the ad's own on/off switch), `budget`, `targeting` or `creative`. Ignore unknown values; new ones can be added.  ### Reading the change  The event never carries old or new values, so read the ad. `platformId` can change when a LinkedIn creative is replaced, while `adId` stays stable.  ### When it does not fire  From the sync, `changes` covers only `name` and `status`. Budget, bid, schedule and targeting edits made outside Zernio, tracking tag edits and history loaded at connect are not announced. Ad rule changes arrive as `ad_rule.triggered`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_ad_updated** | [**WebhookPayloadAdUpdated**](WebhookPayloadAdUpdated.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_ad_video_processed

> on_ad_video_processed(webhook_payload_ad_video_processed)
Ad video processed event

Meta finished processing a video uploaded with `async: true` on `POST /v1/ads/videos`.  ### Payload notes  `video.status` is `ready` (reference it as `video.id` on the create endpoints) or `error`, with `video.error` carrying the reason.  ### When it fires  Fires once per upload, when the video leaves `processing`. Zernio polls every 10 seconds for about 13 minutes; after that no event is sent, so read `GET /v1/ads/videos/{videoId}` for long videos. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_ad_video_processed** | [**WebhookPayloadAdVideoProcessed**](WebhookPayloadAdVideoProcessed.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_analytics_synced

> on_analytics_synced(webhook_payload_analytics_synced)
Analytics synced event

One connected account's analytics sync cycle completed successfully.  ### Payload notes  It is a trigger: no metrics and no cursor. On receipt, call `GET /v1/analytics/delta` with your own last `nextCursor` to read what changed across every account.  ### When it fires  Per account, per successful sync cycle, roughly hourly. It does not fire for a failed or skipped cycle, an inactive or disconnected account, or a platform without analytics sync.  ### Empty page  The feed is a materialized view, so an immediate read can return an empty `data` array. Re-poll with the same cursor. Advancing on an empty page can lose changes permanently.  ### Use a dedicated endpoint  Volume is about one event per account per hour. The consecutive-failure count is shared by every event on an endpoint, so an outage here can disable it and silence events like `post.published`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_analytics_synced** | [**WebhookPayloadAnalyticsSynced**](WebhookPayloadAnalyticsSynced.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_api_changelog_published

> on_api_changelog_published(webhook_payload_api_changelog_published)
API changelog entry published event

An entry was published to the API changelog when a change to the OpenAPI spec went live.  ### Who receives it  It belongs to no profile or account. Every active endpoint subscribed to it receives it; endpoints scoped with `profileIds` or `accountIds` do not. One subscription per integration is enough.  ### Payload notes  `entry.type`, `entry.message` (the announcement), `entry.url`, `entry.specVersion`, `entry.impact` (`action_required`, `additive` or `none`) and `entry.changes` (the spec diff as data).  ### How to act  Automate on `impact`, `changes` and `type`; read `message` for the reason. `GET /v1/changelog` lists entries newest first, to back-fill after downtime. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_api_changelog_published** | [**WebhookPayloadApiChangelogPublished**](WebhookPayloadApiChangelogPublished.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_automation_action_applied

> on_automation_action_applied(webhook_payload_automation_action)
Automation action applied event

An automation changed something, such as an ad set paused or a budget raised.  ### Payload notes  `previous` and `target` carry the value before and the value set. Each action sends one event; dedupe on `id`, which stays the same if the event is sent again. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_automation_action** | [**WebhookPayloadAutomationAction**](WebhookPayloadAutomationAction.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_automation_action_failed

> on_automation_action_failed(webhook_payload_automation_action)
Automation action failed event

An automation change failed or was refused; `reason` says why.  ### Skipped changes  A change refused before any platform call has `status: skipped`, for example no live ads or a budget at its limit. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_automation_action** | [**WebhookPayloadAutomationAction**](WebhookPayloadAutomationAction.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_automation_action_unknown

> on_automation_action_unknown(webhook_payload_automation_action)
Automation action unknown event

The platform did not answer, so it is unknown whether the automation's change happened.  ### What happens next  The next check reads the object back and sends `applied` or `failed`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_automation_action** | [**WebhookPayloadAutomationAction**](WebhookPayloadAutomationAction.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_automation_alert_escalated

> on_automation_alert_escalated(webhook_payload_automation_alert)
Automation alert escalated event

An open alert's `critical` conditions held.  ### When it fires  Sent once per episode. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_automation_alert** | [**WebhookPayloadAutomationAlert**](WebhookPayloadAutomationAlert.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_automation_alert_opened

> on_automation_alert_opened(webhook_payload_automation_alert)
Automation alert opened event

An object matched the rule's conditions for `confirmChecks` runs in a row and its action was recorded.  ### When it fires  Sent once per episode. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_automation_alert** | [**WebhookPayloadAutomationAlert**](WebhookPayloadAutomationAlert.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_automation_alert_resolved

> on_automation_alert_resolved(webhook_payload_automation_alert)
Automation alert resolved event

An open alert ended; `reason` says which way.  ### Reasons  Its conditions cleared, a pause or reactivation applied, the rule changed, or nothing checked the object for 7 days. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_automation_alert** | [**WebhookPayloadAutomationAlert**](WebhookPayloadAutomationAlert.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_automation_check_completed

> on_automation_check_completed(webhook_payload_automation_check_completed)
Automation check completed event

One scheduled check of an automation finished, including checks where nothing matched.  ### Payload notes  `automation.kind` names the product: `ad_rule` today, more as other automations move onto the same engine. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_automation_check_completed** | [**WebhookPayloadAutomationCheckCompleted**](WebhookPayloadAutomationCheckCompleted.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_balance_charged

> on_balance_charged(webhook_payload_balance_charged)
Balance charged event

Balance billing only. Funds were added to the balance by card: by someone (`trigger: manual`) or by the auto top-up rule (`trigger: auto_top_up`).  ### When it fires  Once per card payment into the balance, when it is credited. Stripe emails the billing owner its receipt for the charge.  ### Payload notes  `topup.amountCents` was added to the balance; the card was charged `topup.chargedCents`, which is that plus `topup.taxCents` (VAT, 0 when none applies). The invoice and receipt are at `GET /v1/balance/top-ups/{topupId}/invoice` and `/receipt`.  ### Who receives it  The billing owner's endpoints, like `balance.low`. Restricted keys need the `money` resource group. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_balance_charged** | [**WebhookPayloadBalanceCharged**](WebhookPayloadBalanceCharged.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_balance_empty

> on_balance_empty(webhook_payload_balance_empty)
Balance empty event

Balance billing only. The balance reached $0 and no auto top-up covered it (auto top-up off, the card declined, or the monthly limit reached), so new pay-per-use (SMS, calls, numbers, X and the rest) answers 402 with `code` until the balance is funded.  ### When it fires  Once per time the balance runs out, within about a minute of the usage that emptied it. Funding the balance and running out again fires it again.  ### Who receives it  The billing owner's endpoints, like `balance.low`. Restricted keys need the `money` resource group.  ### How to act  Send the user to `fundingUrl`, or, for `usage_limit_reached`, raise `monthlyLimitCents` with `PATCH /v1/balance/auto-recharge`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_balance_empty** | [**WebhookPayloadBalanceEmpty**](WebhookPayloadBalanceEmpty.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_balance_low

> on_balance_low(webhook_payload_balance_low)
Balance low event

Balance billing only. The balance dropped below the low-balance alert set on auto top-up (`alertBelowCents` on `GET /v1/balance/auto-recharge`).  ### When it fires  Once per drop below the threshold; a balance back at or above it re-arms the next one. It does not fire when an auto top-up is already covering the drop, and never when no alert is set.  ### Who receives it  It belongs to the billing owner, not to a profile or account: endpoints scoped with `profileIds` or `accountIds` do not receive it. Restricted keys need the `money` resource group.  ### How to act  Send the user to `fundingUrl` (Billing with the Add funds drawer open), or add funds through the API. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_balance_low** | [**WebhookPayloadBalanceLow**](WebhookPayloadBalanceLow.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_branded_calling_identity_action_required

> on_branded_calling_identity_action_required(on_branded_calling_identity_action_required_request)
Caller identity action required event

A Branded Calling caller identity is waiting on you; `reason` says what.  ### When it fires  Every `action_required` is paired with a `status_updated`.  ### Reasons  - `changes_requested`: answer the review with `PATCH`. - `email_code`: confirm the code the carrier emailed the authorizer. - `rejected`: fix and `PATCH`. - `expired`: resubmit.  ### Infringement claim  `infringement_claim`: a third party filed a trademark or impersonation claim and the carrier suspended the identity. Calls show a plain number and the monthly fee pauses until it is resolved.  Reply to our email with evidence that the name and logo are yours. If the claim is upheld, the identity is rejected for good. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_branded_calling_identity_action_required_request** | [**OnBrandedCallingIdentityActionRequiredRequest**](OnBrandedCallingIdentityActionRequiredRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_branded_calling_identity_status_updated

> on_branded_calling_identity_status_updated(on_branded_calling_identity_status_updated_request)
Caller identity status updated event

A Branded Calling caller identity changed status.  ### When it fires  Fires once per transition of the identity's `status`, the value `GET /v1/branded-calling/identities/{id}` returns. Never on a re-check that found nothing new.  ### Statuses  `requested`, `changes_requested`, `rejected` (`reason` says why), `pending_email_verification`, `in_review`, `verified` (live for a year, attach numbers), `suspended` (infringement claim open), `expired`, `permanently_rejected`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_branded_calling_identity_status_updated_request** | [**OnBrandedCallingIdentityStatusUpdatedRequest**](OnBrandedCallingIdentityStatusUpdatedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_branded_calling_number_status_updated

> on_branded_calling_number_status_updated(on_branded_calling_number_status_updated_request)
Branded number status updated event

A number attached to a Branded Calling identity changed vetting status.  ### When it fires  Only starts once the identity is `verified` and you attached numbers. A batch is vetted as a unit; each number reports its own status.  ### Statuses  `submitted`, `in_review`, `verified` (calls from it show the identity), `unsuccessful` (refused; detach and re-add to retry), `suspended`, `expired`, `permanently_rejected` (can never be branded again). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_branded_calling_number_status_updated_request** | [**OnBrandedCallingNumberStatusUpdatedRequest**](OnBrandedCallingNumberStatusUpdatedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_calendar_event_created

> on_calendar_event_created(webhook_payload_calendar_event)
Calendar event created

An event was added to a watched calendar of a connected mailbox, by the user, an invitation or the API. Google watches every calendar the user shows (up to 25), Outlook the default calendar; `calendarId` names it.  ### Platform notes  On Microsoft the change is pushed seconds after it happens. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_calendar_event** | [**WebhookPayloadCalendarEvent**](WebhookPayloadCalendarEvent.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_calendar_event_deleted

> on_calendar_event_deleted(webhook_payload_calendar_event)
Calendar event deleted

An event was deleted from a watched calendar.  ### Platform notes  On Google, a cancelled event counts as deleted. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_calendar_event** | [**WebhookPayloadCalendarEvent**](WebhookPayloadCalendarEvent.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_calendar_event_updated

> on_calendar_event_updated(webhook_payload_calendar_event)
Calendar event updated

An event on a watched calendar changed: its time, details or participants' answers. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_calendar_event** | [**WebhookPayloadCalendarEvent**](WebhookPayloadCalendarEvent.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_call_ended

> on_call_ended(webhook_payload_call_ended)
Call ended event

A phone or WhatsApp call ended; carries duration, end reason and a zero-markup cost breakdown.  ### Payload notes  `durationSeconds`; `endReason` is `hangup`, `no_answer`, `rejected` or `error`; `call.billing` holds Meta cost, Telnyx cost, recording surcharge and total. Costs are pass-through, with no margin.  ### When it fires  Unanswered, busy and rejected calls end here too. Branch on `endReason`; `call.failed` is for hard errors.  ### Recordings  With recording enabled, the payload carries `recordingUrl`, a signed URL expiring at `recordingExpiresAt`. Fetch a fresh one with `GET /v1/calls/{id}/recording` and `call.id`.  ### Missed-call follow-up  Check for `endReason: \"no_answer\"`, then text the caller over the linked `conversationId`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_call_ended** | [**WebhookPayloadCallEnded**](WebhookPayloadCallEnded.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_call_failed

> on_call_failed(webhook_payload_call_failed)
Call failed event

A call failed with a hard error before or during bridging, for example the destination rejected the SIP INVITE.  ### Payload notes  Carries the upstream error `code` and `message`, for example when Meta rejected the connect or Telnyx returned an error. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_call_failed** | [**WebhookPayloadCallFailed**](WebhookPayloadCallFailed.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_call_permission_request

> on_call_permission_request(webhook_payload_call_permission_request)
Call permission request reply event

A WhatsApp user accepted or rejected your call-permission request.  ### When it fires  Independent of any call: it reports a reply to a permission prompt. Meta permits a business-initiated call only after the consumer taps Allow, and the accept can land days before the call.  ### Payload notes  `response` is `accept` or `reject`. Also carries the user's number, whether the grant is permanent, and the expiry when it is not. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_call_permission_request** | [**WebhookPayloadCallPermissionRequest**](WebhookPayloadCallPermissionRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_call_received

> on_call_received(webhook_payload_call_received)
Call received event

An inbound phone or WhatsApp call reached your number, or an outbound WhatsApp call was placed.  ### When it fires  Fires at ring time, before anyone answers; an unanswered call still emits it, then `call.ended` with `endReason: \"no_answer\"`. Outbound WhatsApp calls fire at origination with `direction: \"outbound\"`. Outbound phone calls never emit it.  ### Payload notes  Carries the Zernio call id, the caller and business numbers, the destination snapshot (`forwardTo`), and `contactId` and `conversationId` to message the caller with the regular send endpoints. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_call_received** | [**WebhookPayloadCallReceived**](WebhookPayloadCallReceived.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_call_recording_ready

> on_call_recording_ready(webhook_payload_call_recording_ready)
Call recording ready event

A call recording is ready to download.  ### When it fires  Only for teams with zero content retention, on calls with recording on, and only while a webhook listens to it. Zernio keeps no recording for these teams, and the copy behind the link expires after about 3 days. Download the file before `recording.expiresAt`.  ### Payload notes  `call.isVoicemail` tells a voicemail from a recorded call. If the recording could not be copied, no event fires and `call.ended` lists it in `callErrors`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_call_recording_ready** | [**WebhookPayloadCallRecordingReady**](WebhookPayloadCallRecordingReady.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_call_transcript_segment

> on_call_transcript_segment(webhook_payload_call_transcript_segment)
Call transcript segment event

One final segment of a live call transcript.  ### When it fires  Only for teams with zero content retention, on calls with transcription on: once per final segment, while the call is live. Zernio stores no transcript for these teams, so it cannot be fetched later. Store each segment when it arrives.  ### Payload notes  `segment.text` is the final text, `segment.confidence` the recognition confidence and `segment.at` when it was transcribed. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_call_transcript_segment** | [**WebhookPayloadCallTranscriptSegment**](WebhookPayloadCallTranscriptSegment.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_budget_depleted

> on_campaign_budget_depleted(webhook_payload_campaign_budget_depleted)
Campaign budget depleted event

A campaign Zernio already tracked ran out of budget. TikTok only.  ### When it fires  Fires once per campaign when its budget runs out, at most once per 6 hours, so a daily budget that runs out again the next day is announced again.  ### When it does not fire  Ads seen for the first time by a sync never fire it.  ### Platform notes  Only TikTok reports this on the ad. Meta and Google keep such ads `ACTIVE`, so they never fire it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_budget_depleted** | [**WebhookPayloadCampaignBudgetDepleted**](WebhookPayloadCampaignBudgetDepleted.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_created

> on_campaign_created(webhook_payload_campaign_created)
Campaign created event

A campaign was created through Zernio (`source: \"zernio\"`) or detected by the sync (`source: \"platform\"`).  ### When it fires  Fires once the campaign row is recorded. A detected campaign arrives up to one sync interval late.  ### When it does not fire  History loaded when an account connects, and campaigns created more than 7 days ago, are never announced. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_created** | [**WebhookPayloadCampaignCreated**](WebhookPayloadCampaignCreated.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_draft_approved

> on_campaign_draft_approved(webhook_payload_campaign_draft)
Campaign draft approved event

You approved a draft version.  ### Effect  The creator can now publish it and submit the post with its `draftId`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_draft** | [**WebhookPayloadCampaignDraft**](WebhookPayloadCampaignDraft.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_draft_rejected

> on_campaign_draft_rejected(webhook_payload_campaign_draft)
Campaign draft rejected event

You rejected a draft version.  ### Effect  It can never back a post, and it gets no new version. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_draft** | [**WebhookPayloadCampaignDraft**](WebhookPayloadCampaignDraft.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_draft_revision_requested

> on_campaign_draft_revision_requested(webhook_payload_campaign_draft)
Campaign draft revision requested event

You asked for changes to a draft version.  ### Comments  `draft.comments` lists your notes, each with `atMs` for the moment of the video it points at, or null for a general note. The creator can upload one new version of it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_draft** | [**WebhookPayloadCampaignDraft**](WebhookPayloadCampaignDraft.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_draft_submitted

> on_campaign_draft_submitted(webhook_payload_campaign_draft)
Campaign draft submitted event

A creator uploaded a draft, or a new version of one, on a campaign with `requireDraftApproval`.  ### Versions  `draft.version` is 1 for a new draft, higher for a new version answering your requested changes, and `draft.revisionOf` names the version it answers. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_draft** | [**WebhookPayloadCampaignDraft**](WebhookPayloadCampaignDraft.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_participant_approved

> on_campaign_participant_approved(webhook_payload_campaign_participant)
Campaign participant approved event

You accepted a creator who asked to join.  ### Effect  They are now `active` and `participant.joinedAt` is set. This event replaces `campaign_participant.joined` for them, so it fires instead of it, never with it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_participant** | [**WebhookPayloadCampaignParticipant**](WebhookPayloadCampaignParticipant.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_participant_denied

> on_campaign_participant_denied(webhook_payload_campaign_participant)
Campaign participant denied event

You turned down a creator who asked to join.  ### Effect  They cannot submit anything to this campaign. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_participant** | [**WebhookPayloadCampaignParticipant**](WebhookPayloadCampaignParticipant.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_participant_joined

> on_campaign_participant_joined(webhook_payload_campaign_participant)
Campaign participant joined event

A creator joined a campaign from their invite link or the open link.  ### When it fires  It fires once per participant, and `participant.joinedAt` says when. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_participant** | [**WebhookPayloadCampaignParticipant**](WebhookPayloadCampaignParticipant.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_participant_pending

> on_campaign_participant_pending(webhook_payload_campaign_participant)
Campaign participant pending event

A creator asked to join a campaign that reviews creators.  ### When it fires  A creator joined from the open link of a campaign whose `joinApproval` is `manual`. They wait as `pending` until you approve or deny them, and they do not take a place under `maxParticipants` while they wait. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_participant** | [**WebhookPayloadCampaignParticipant**](WebhookPayloadCampaignParticipant.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_participant_removed

> on_campaign_participant_removed(webhook_payload_campaign_participant)
Campaign participant removed event

You removed a participant from the campaign.  ### When it does not fire  Removing a participant twice fires the event once. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_participant** | [**WebhookPayloadCampaignParticipant**](WebhookPayloadCampaignParticipant.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_participant_suspended

> on_campaign_participant_suspended(webhook_payload_campaign_participant)
Campaign participant suspended event

You suspended a participant.  ### Effect  They can no longer connect accounts or submit posts to this campaign. Posts they already submitted keep earning until you reject them. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_participant** | [**WebhookPayloadCampaignParticipant**](WebhookPayloadCampaignParticipant.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_payout_failed

> on_campaign_payout_failed(webhook_payload_campaign_payout)
Campaign payout failed event

A payout through Zernio did not reach the creator.  ### When it fires  Stripe refused it, it stayed unconfirmed for 24 hours, or it was reversed. The amount is payable again, minus anything a rejection claws back. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_payout** | [**WebhookPayloadCampaignPayout**](WebhookPayloadCampaignPayout.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_payout_payable

> on_campaign_payout_payable(webhook_payload_campaign_payout)
Campaign payout payable event

A participant's held earnings matured and became payable.  ### Payload notes  `payout.payableCents` is the participant's whole payable balance, the amount to pay when you pay from your own rails. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_payout** | [**WebhookPayloadCampaignPayout**](WebhookPayloadCampaignPayout.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_payout_settled

> on_campaign_payout_settled(webhook_payload_campaign_payout)
Campaign payout settled event

A payout to a participant was recorded.  ### Payload notes  `payout.settlement` holds the amount and the reference. `recorded` is true when the money moved outside Zernio. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_payout** | [**WebhookPayloadCampaignPayout**](WebhookPayloadCampaignPayout.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_sample_approved

> on_campaign_sample_approved(webhook_payload_campaign_sample)
Campaign sample approved event

You approved a sample request.  ### Discount code  `sample.discountCode` is the single-use, 100% off code created in your store for that product. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_sample** | [**WebhookPayloadCampaignSample**](WebhookPayloadCampaignSample.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_sample_declined

> on_campaign_sample_declined(webhook_payload_campaign_sample)
Campaign sample declined event

You declined a sample request.  ### Effect  `sample.declineReason` says why. The creator can ask for the same product again. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_sample** | [**WebhookPayloadCampaignSample**](WebhookPayloadCampaignSample.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_sample_requested

> on_campaign_sample_requested(webhook_payload_campaign_sample)
Campaign sample requested event

A creator asked for one of the campaign's `sampleProducts`, with a shipping address. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_sample** | [**WebhookPayloadCampaignSample**](WebhookPayloadCampaignSample.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_sample_shipped

> on_campaign_sample_shipped(webhook_payload_campaign_sample)
Campaign sample shipped event

You marked an approved sample as shipped.  ### Tracking  `sample.trackingUrl` is set when you gave one. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_sample** | [**WebhookPayloadCampaignSample**](WebhookPayloadCampaignSample.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_submission_approved

> on_campaign_submission_approved(webhook_payload_campaign_submission)
Campaign submission approved event

You approved a submission.  ### Earnings  What the submission earned so far moves to owed with the campaign hold. Later earnings post straight to owed. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_submission** | [**WebhookPayloadCampaignSubmission**](WebhookPayloadCampaignSubmission.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_submission_flagged

> on_campaign_submission_flagged(webhook_payload_campaign_submission)
Campaign submission flagged event

A submission gained a fraud flag it did not carry before, at submission or on a later sync.  ### Flags  Flags include `duplicate_post`, `view_spike`, `low_authenticity` and `x_read_cap` (the campaign's X read budget is spent). `submission.flags` lists every flag it carries. Zernio never rejects on its own; the decision is yours. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_submission** | [**WebhookPayloadCampaignSubmission**](WebhookPayloadCampaignSubmission.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_submission_pending_review

> on_campaign_submission_pending_review(webhook_payload_campaign_submission)
Campaign submission pending review event

A submission is ready for your review.  ### When it fires  A CPM submission reached `minViewsToEarn`, a pool submission reached `minViewsToQualify`, and per post submissions arrive here after their first accrual. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_submission** | [**WebhookPayloadCampaignSubmission**](WebhookPayloadCampaignSubmission.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_submission_received

> on_campaign_submission_received(webhook_payload_campaign_submission)
Campaign submission received event

A creator submitted a post to a campaign, Zernio opened its tracking window and took the first view sample. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_submission** | [**WebhookPayloadCampaignSubmission**](WebhookPayloadCampaignSubmission.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_submission_rejected

> on_campaign_submission_rejected(webhook_payload_campaign_submission)
Campaign submission rejected event

You rejected a submission and its tracking window was cancelled.  ### Earnings  Its unsettled earnings go back to the campaign budget. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_submission** | [**WebhookPayloadCampaignSubmission**](WebhookPayloadCampaignSubmission.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_campaign_updated

> on_campaign_updated(webhook_payload_campaign_updated)
Campaign updated event

A campaign was edited through Zernio (`source: \"zernio\"`), or outside Zernio and detected by the sync (`source: \"platform\"`).  ### When it fires  Fires after the platform and Zernio both accepted the edit. Outside edits arrive up to one sync interval late, and only to the user whose sync saw them.  ### Deduplication  Events are not deduplicated, so every edit is announced. Use the event `id` to drop repeats.  ### Payload notes  `changes` lists the edited fields: `name`, `status` (the campaign's own on/off switch), `budget`, `bid` or `settings`. Ignore unknown values. It never carries old or new values, so read the campaign.  ### What the sync detects  From the sync, `changes` covers only `name`, `status` and `schedule`. Schedule is detected only on Google, LinkedIn, Pinterest and OpenAI Ads.  ### When it does not fire  Budget edits made outside Zernio and history loaded at connect are not announced. Ad set edits arrive as `ad_set.updated`. Ad rule changes arrive as `ad_rule.triggered`.  ### Google sub-resources  Edits to ad schedule, targeting, negative keywords, conversion goals, assets, asset groups and listing group filters are not announced. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_campaign_updated** | [**WebhookPayloadCampaignUpdated**](WebhookPayloadCampaignUpdated.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_comment_received

> on_comment_received(webhook_payload_comment)
Comment received event

A new comment arrived on a tracked post.  ### Platform notes  Delivered for Instagram, Facebook, Threads, YouTube, LinkedIn, Bluesky, Reddit and TikTok. X/Twitter does not fire it. TikTok needs an account connected through the TikTok for Business app.  ### Delivery timing  Instagram, Facebook, Threads and TikTok arrive in real time from the platform's webhook. The rest are poll-driven, so delivery is not instant.  ### Live comments  On Instagram, `comment.isLive: true` marks a comment made during a live broadcast. The key is absent on every other comment.  ### Ads  `comment.ad` is present only on comments made on paid content, so `if (comment.ad)` filters ad-driven comments.  ### Ad fields  Instagram carries `ad.id` and `ad.title`. Facebook carries `ad.promotionStatus`: `active` for boosted organic posts, `ineligible` for dark post creatives.  ### Instagram author profile  Comments may carry `comment.author.instagramProfile` (`isFollower`, `isFollowing`, `followerCount`, `isVerified`). An absent object means unknown, never \"not a follower\".  ### Why the profile is often absent  Meta reveals the follow relationship only for people who have messaged the account, and commenting does not grant that consent. The object is absent for most first-time commenters. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_comment** | [**WebhookPayloadComment**](WebhookPayloadComment.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_commerce_order_created

> on_commerce_order_created(webhook_payload_commerce_order)
Commerce order created event

An order was placed in the store.  ### Payload notes  `resource.status` is its normalized state at that moment. Read the order with `GET /v1/commerce/orders/{orderId}?accountId=...`. Fires once per Zernio account. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_commerce_order** | [**WebhookPayloadCommerceOrder**](WebhookPayloadCommerceOrder.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_commerce_order_refunded

> on_commerce_order_refunded(webhook_payload_commerce_order)
Commerce order refunded event

A refund was issued on an order.  ### Payload notes  `resource.id` is the order id, not the refund id. `resource.status` and `resource.platformStatus` are `null`. A `commerce.order.updated` usually follows for the same change. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_commerce_order** | [**WebhookPayloadCommerceOrder**](WebhookPayloadCommerceOrder.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_commerce_order_updated

> on_commerce_order_updated(webhook_payload_commerce_order)
Commerce order updated event

An order changed in the store, such as payment, fulfilment, cancellation or edits.  ### Payload notes  `resource.status` is the new state. Refunds also fire it. Fires once per Zernio account connected to the store. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_commerce_order** | [**WebhookPayloadCommerceOrder**](WebhookPayloadCommerceOrder.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_commerce_product_created

> on_commerce_product_created(webhook_payload_commerce_product)
Commerce product created event

A product was created in a connected Shopify store or WooCommerce site.  ### Payload notes  `resource.id` is the store's product id. Read the product with `GET /v1/commerce/products/{productId}?accountId=...`. Fires once per Zernio account connected to the store. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_commerce_product** | [**WebhookPayloadCommerceProduct**](WebhookPayloadCommerceProduct.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_commerce_product_deleted

> on_commerce_product_deleted(webhook_payload_commerce_product)
Commerce product deleted event

A product was deleted in the store.  ### Payload notes  `resource.status` and `resource.platformStatus` are `null`. Fires once per Zernio account connected to the store. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_commerce_product** | [**WebhookPayloadCommerceProduct**](WebhookPayloadCommerceProduct.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_commerce_product_updated

> on_commerce_product_updated(webhook_payload_commerce_product)
Commerce product updated event

A product changed in the store, or WooCommerce restored it from the trash.  ### Payload notes  Fields, status, variants or prices changed; read the product for what. There is no restored event. Fires once per Zernio account connected to the store. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_commerce_product** | [**WebhookPayloadCommerceProduct**](WebhookPayloadCommerceProduct.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_contact_deleted

> on_contact_deleted(webhook_payload_contact)
Contact deleted

A contact was deleted in Google Contacts or Outlook.  ### Effect  Zernio removes its email channels for that account; the contact stays when other channels remain. It arrives up to 15 minutes after the change, from the sync. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_contact** | [**WebhookPayloadContact**](WebhookPayloadContact.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_contact_field_changed

> on_contact_field_changed(webhook_payload_contact_field_changed)
Contact field changed event

A contact custom field changed value; `field` is the field slug.  ### When it fires  Once per custom field whose value a write changed. Writing the current value fires nothing.  ### Payload notes  `previousValue` is `null` when the field was not set. `value` is `null` when it was removed. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_contact_field_changed** | [**WebhookPayloadContactFieldChanged**](WebhookPayloadContactFieldChanged.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_contact_tag_added

> on_contact_tag_added(webhook_payload_contact_tag)
Contact tag added event

A tag was added to a contact by the API, a workflow `add_tag` node or a comment-automation click.  ### When it fires  Once per tag a write actually added. Re-adding a tag the contact already has fires nothing.  ### When it does not fire  Creating a contact with tags fires nothing. Only changes to an existing contact do. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_contact_tag** | [**WebhookPayloadContactTag**](WebhookPayloadContactTag.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_contact_tag_removed

> on_contact_tag_removed(webhook_payload_contact_tag)
Contact tag removed event

A tag was removed from a contact.  ### When it fires  Once per tag a write actually removed. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_contact_tag** | [**WebhookPayloadContactTag**](WebhookPayloadContactTag.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_contact_updated

> on_contact_updated(webhook_payload_contact)
Contact updated

A contact sync added or changed a contact; `contact.id` is the Zernio contact id.  ### When it fires  It fires from the sync of a Google Contacts or Outlook account, which runs every 15 minutes, so up to 15 minutes after the change. It also fires when a WhatsApp coexistence address book adds or renames a contact. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_contact** | [**WebhookPayloadContact**](WebhookPayloadContact.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_conversation_control_changed

> on_conversation_control_changed(webhook_payload_conversation_control_changed)
Conversation control changed event

Control of a conversation moved: Meta Business Agent on WhatsApp, or Meta's conversation routing on Facebook and Instagram (`messaging_handovers`). On Instagram, Conversation Routing replaced the Handover Protocol in October 2025 and kept its thread-control events.  ### Owner values  `control.owner` is `ai_agent` (Meta Business Agent, WhatsApp), `app` (you) or `other` (a WhatsApp partner app, or a receiver such as Page Inbox on Messenger and Instagram).  ### Control fields  `control.previousOwner` is `null` when no handover touched the thread. `control.ownerAppId` is the new owner's Meta app id when named (Page Inbox is `263902037430900`). `control.metadata` is the transferring app's note, verbatim.  ### WhatsApp  Meta Business Agent took the conversation, handed it to you, or another partner app took it. While `ai_agent` owns it, its replies arrive on `message.sent` with `source: \"meta_business_agent\"`.  ### Taking control on WhatsApp  Sending any message through the inbox takes control back. To hand it to the agent without sending, call `POST /v1/inbox/conversations/{conversationId}/thread-control` with `action: \"release\"`.  ### Facebook and Instagram  Meta sent Zernio a `pass_thread_control` (another app passed the thread to you) or `take_thread_control` (another app took it from you) event. It fires once per change of the stored owner.  It does not fire on `release` or when two other apps move a thread between them (Meta sends nothing), nor for your own thread-control calls (their response carries the new owner).  While you are not the owner, sends answer `409` `not_thread_owner`.  ### Taking control on Facebook and Instagram  Call `POST /v1/inbox/conversations/{conversationId}/thread-control` with `action: \"take\"`, or `\"request\"` to ask the owner to pass it. Both answer 400 `platform_not_supported` on Instagram Login connections.  Meta accepts `take` only when the account has a default app set in conversation routing and the business has allowed Zernio to take control of conversations; otherwise it answers code 27.  ### When it does not fire  A repeat report of the same owner fires nothing. A `request` changes nothing until the owner passes the thread.  ### Standby messages  While another app owns the conversation, inbound messages arrive on `message.received` with `metadata.standby: true`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_conversation_control_changed** | [**WebhookPayloadConversationControlChanged**](WebhookPayloadConversationControlChanged.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_conversation_started

> on_conversation_started(webhook_payload_conversation_started)
Conversation started event

A new conversation began between a connected account and a contact, in either direction, on any DM platform.  ### When it fires  Once per conversation, the first time it appears. Covers Instagram, Messenger, WhatsApp, Telegram, X, Reddit, Bluesky, TikTok, SMS, RCS, iMessage, Slack, LINE, WeChat and email.  ### When it does not fire  DM history replayed when an Instagram or Facebook account connects never fires it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_conversation_started** | [**WebhookPayloadConversationStarted**](WebhookPayloadConversationStarted.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_conversion_received

> on_conversion_received(webhook_payload_conversion)
Conversion received event

Zernio stored an event: one sent to `POST /v1/events` or `POST /v1/ads/conversions`, or one a connected source sent for you (a lead form lead, a Shopify or WooCommerce order, a HubSpot deal). It fires again when a newer version of the same event is stored, such as an order that changed.  `conversion` has the fields of `GET /v1/events/{eventId}`, plus `source`, `campaign` (the campaign the event counts for, or null) and `campaignMatch` (why there is none). Personal data is never sent: `hasEmail`, `hasPhone` and `hasExternalId` only say what the event carried.  ### Deduplication  The event `id` follows the stored event and its version, so a resend of the same version carries the same `id`. Deduplicate on it.  ### Not sent for  Test events (they are never stored), corrections made with `PATCH` or `DELETE /v1/events/{eventId}`, and the hourly re-match that ties an earlier event to its campaign. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_conversion** | [**WebhookPayloadConversion**](WebhookPayloadConversion.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_creator_campaign_budget_exhausted

> on_creator_campaign_budget_exhausted(webhook_payload_creator_campaign)
Creator campaign budget exhausted event

A campaign's earnings reached its budget.  ### When it fires  Nothing more accrues until budget is freed. It fires once per campaign. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_creator_campaign** | [**WebhookPayloadCreatorCampaign**](WebhookPayloadCreatorCampaign.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_creator_campaign_closed

> on_creator_campaign_closed(webhook_payload_creator_campaign)
Creator campaign closed event

A campaign closed, either because you closed it or because `endsAt` passed.  ### When it fires  After `endsAt`, the campaign closes once every tracking window had its final read. A pool campaign is split among participants at this moment. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_creator_campaign** | [**WebhookPayloadCreatorCampaign**](WebhookPayloadCreatorCampaign.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_email_bounced

> on_email_bounced(webhook_payload_email_bounced)
Email bounced

A delivery failure report for mail the mailbox sent arrived: the receiving server refused it for a recipient. Fires for every send from the mailbox, once per failed recipient. Delayed-delivery warnings and out-of-office replies do not fire it.  Act on `recommendedAction`: `remove` means the address does not take mail. Refusals on the sending side (`auth_failure`, `blocklisted`, `spam_blocked`, `policy_blocked`) never say `remove`. The report also arrives as `message.received`, and it does not count as a reply for `email.thread_replied`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_email_bounced** | [**WebhookPayloadEmailBounced**](WebhookPayloadEmailBounced.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_email_deleted

> on_email_deleted(webhook_payload_email_deleted)
Email deleted

A message was deleted from the mailbox for good. Moving it to Trash is `email.updated` with `folder: \"trash\"`. IMAP mailboxes do not send it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_email_deleted** | [**WebhookPayloadEmailDeleted**](WebhookPayloadEmailDeleted.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_email_link_clicked

> on_email_link_clicked(webhook_payload_email_link_clicked)
Email link clicked

A recipient followed a link of a message sent with `trackLinks: true`. Every http(s) link in the html was rewritten to a Zernio redirect that records the click and sends the reader on to `click.url`.  Security scanners in corporate mail gateways sometimes follow links on delivery, which reports as a click. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_email_link_clicked** | [**WebhookPayloadEmailLinkClicked**](WebhookPayloadEmailLinkClicked.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_email_opened

> on_email_opened(webhook_payload_email_opened)
Email opened

A mail client loaded the open pixel of a message sent with `trackOpens: true`.  Opens are a signal, not proof of reading:  - Gmail and Apple Mail fetch images through their own proxies, some as soon as the mail arrives. - Clients that block images never report an open. - The sender viewing the message in their own Sent folder counts too.  Repeat fetches within 10 seconds raise `count` without firing again. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_email_opened** | [**WebhookPayloadEmailOpened**](WebhookPayloadEmailOpened.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_email_send_failed

> on_email_send_failed(webhook_payload_email_send_failed)
Scheduled email failed

A send scheduled with `scheduledFor` could not leave at its time. Nothing reached the recipients. `error` says why, for example the mailbox was disconnected, the daily send cap was reached or the provider refused the mail. The send stays listed with `status: failed`; schedule it again to retry. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_email_send_failed** | [**WebhookPayloadEmailSendFailed**](WebhookPayloadEmailSendFailed.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_email_sent

> on_email_sent(webhook_payload_email_sent)
Email sent

A mail left through the email API. Exactly one event per mail, whichever path sent it: `source` is `send`, `reply`, `forward`, `draft` or `scheduled`. A scheduled draft carries both `scheduleId` and `draftId`.  Use it to record sends in your own system with the `metadata` you passed. The sent copy also arrives as `message.sent` in the inbox. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_email_sent** | [**WebhookPayloadEmailSent**](WebhookPayloadEmailSent.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_email_thread_replied

> on_email_thread_replied(webhook_payload_email_thread_replied)
Email thread replied

Mail from someone other than the mailbox arrived in the thread of a message sent with `trackReplies: true`. Works on text and html sends. Auto-replies count as replies; bounce reports do not and fire `email.bounced` instead.  `reply.clean.text` is the reply without the quoted history, so an agent can act on it without reading the message. The reply also arrives as `message.received` with its full content. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_email_thread_replied** | [**WebhookPayloadEmailThreadReplied**](WebhookPayloadEmailThreadReplied.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_email_updated

> on_email_updated(webhook_payload_email_updated)
Email updated

A message in the mailbox changed: it was read or marked unread, starred or flagged, labelled or categorized, archived, trashed or moved. Covers the Inbox, and Sent on Gmail. A change can arrive more than once; key on `email.messageId`.  Gmail reports exactly what changed in `changes`. Outlook reports the message as it is now, with `changes: null`. A message deleted for good fires `email.deleted` instead. IMAP mailboxes do not send it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_email_updated** | [**WebhookPayloadEmailUpdated**](WebhookPayloadEmailUpdated.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_file_created

> on_file_created(webhook_payload_file)
File created

A file the account can reach was created in Google Drive or OneDrive.  ### Platform notes  A folder counts as a file. The event is pushed seconds after the change. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_file** | [**WebhookPayloadFile**](WebhookPayloadFile.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_file_deleted

> on_file_deleted(webhook_payload_file)
File deleted

A file the account could reach was deleted or moved to the trash. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_file** | [**WebhookPayloadFile**](WebhookPayloadFile.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_file_picked

> on_file_picked(webhook_payload_file_picked)
Files picked

The user picked files in a picker session; `picker.files` lists each one's `id`, `name`, `mimeType` and `kind`.  ### When it fires  It fires when the user finishes a hosted picker session (`POST /v1/files/picker-sessions`) and picks at least one file. Not sent on cancel. The files are readable from then on. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_file_picked** | [**WebhookPayloadFilePicked**](WebhookPayloadFilePicked.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_file_updated

> on_file_updated(webhook_payload_file)
File updated

A file the account can reach was changed, renamed or moved. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_file** | [**WebhookPayloadFile**](WebhookPayloadFile.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_lead_received

> on_lead_received(webhook_payload_lead)
Lead received event

A new lead was submitted against a Meta Lead Gen (Instant) form or a TikTok Instant Form (both pushed by the network), or a Google Ads or LinkedIn lead form (read every 15 minutes). `lead.platform` names the network.  Leads older than 7 days when Zernio first reads them are stored without this event.  ### Payload notes  `lead.fields` maps question key to answer; multiple-choice values are the option key (for example `k1`), not the display label.  ### Provenance  `lead.formId`, `lead.adId` and `lead.campaignId` give provenance. `lead.adId` is null for organic or test leads.  ### Consents  `lead.consents` lists the answer to every custom disclaimer checkbox, for example `{ \"checkboxKey\": \"call_consent\", \"isChecked\": true }`. Route call and SMS consent into your CRM from it. Empty when the form has no checkboxes.  ### Checkbox keys  When no key was set on the checkbox, Meta derives `checkboxKey` from its text, so match on the full key. `GET /v1/ads/leads` and `GET /v1/ads/lead-forms/{formId}/leads` return the same array.  ### Deduplication  Deduplicate on `lead.leadgenId` (Meta's lead id) or the event `id`.  ### Routing  `account.profileId` names the Zernio profile of the Facebook account that received the lead, for multi-tenant routing. Always present, `null` only when no profile is on record.  ### Requires ads enabled  Needs ads enabled on the team. Zernio asks for `leads_retrieval` at Facebook consent only then; without it Meta refuses the Page's `leadgen` subscription. Accounts connected earlier need a reconnect.  ### Lost subscription  A Page can lose its `leadgen` subscription while other events keep arriving. `leadgen: false` (with a `warning`) on the Page's webhook subscription means leads are not reaching Zernio; re-subscribe the Page. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_lead** | [**WebhookPayloadLead**](WebhookPayloadLead.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_mention_received

> on_mention_received(webhook_payload_mention)
Mention received event

A connected Instagram, Facebook or LinkedIn account was mentioned in a post, caption or comment.  ### When it fires  Once per mention, the first time Zernio sees it. Delivery is at most once: reconcile with `GET /v1/inbox/mentions`.  - Instagram and Facebook arrive in real time from the platform's webhook. - LinkedIn arrives from its webhook or from polling, so delivery can take minutes. A newly connected account can receive mentions from the last 48 hours once.  ### Payload notes  Carries the same fields as `GET /v1/inbox/mentions`. Fields a platform does not provide are null. A LinkedIn mention found by polling for a team that does not retain content has no author, and an Instagram mention has no content if the live read fails. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_mention** | [**WebhookPayloadMention**](WebhookPayloadMention.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_message_deleted

> on_message_deleted(webhook_payload_message_deleted)
Message deleted event

A sender deleted (unsent) a message on Instagram or WhatsApp.  ### Platform notes  Instagram reports incoming unsends. WhatsApp reports both directions, including business deletions through the Cloud API or a Coexistence app. `message.direction` tells them apart.  ### Payload notes  The payload keeps the pre-delete `text` and `attachments` for moderation, compliance or archival. The Zernio dashboard does not show this content. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_message_deleted** | [**WebhookPayloadMessageDeleted**](WebhookPayloadMessageDeleted.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_message_delivered

> on_message_delivered(webhook_payload_message_delivery_status)
Message delivered event

An outgoing message was delivered to the recipient on WhatsApp, Facebook Messenger, SMS, RCS or iMessage.  ### Platform notes  On WhatsApp, `pricing` and `billingConversation` carry Meta's billing context for the message. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_message_delivery_status** | [**WebhookPayloadMessageDeliveryStatus**](WebhookPayloadMessageDeliveryStatus.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_message_edited

> on_message_edited(webhook_payload_message_edited)
Message edited event

A sender edited a previously sent message on Instagram, Facebook Messenger, Telegram or WhatsApp.  ### Payload notes  `editHistory` holds every prior version, oldest first. `message.text` is the latest version. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_message_edited** | [**WebhookPayloadMessageEdited**](WebhookPayloadMessageEdited.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_message_failed

> on_message_failed(webhook_payload_message_delivery_status)
Message delivery failed event

An outgoing message failed to deliver on WhatsApp, SMS, RCS or iMessage.  ### Payload notes  `error` carries `code`, `title` and `message` from the platform, for example `131026` for an unreachable WhatsApp recipient. On SMS it carries the carrier's error code. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_message_delivery_status** | [**WebhookPayloadMessageDeliveryStatus**](WebhookPayloadMessageDeliveryStatus.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_message_played

> on_message_played(webhook_payload_message_delivery_status)
Message played event

A WhatsApp recipient played a voice message you sent, reported the first time they play it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_message_delivery_status** | [**WebhookPayloadMessageDeliveryStatus**](WebhookPayloadMessageDeliveryStatus.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_message_read

> on_message_read(webhook_payload_message_delivery_status)
Message read event

An outgoing message was read by the recipient on WhatsApp, Facebook Messenger, Instagram or RCS. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_message_delivery_status** | [**WebhookPayloadMessageDeliveryStatus**](WebhookPayloadMessageDeliveryStatus.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_message_received

> on_message_received(webhook_payload_message)
Message received event

A new message arrived in the inbox; `message.text`, `message.attachments[]` and `message.sender` describe it.  ### Standby  While another app owns the conversation it carries `metadata.standby: true`. Zernio runs no workflow or keyword automation on it. A bot must skip standby messages, or on WhatsApp it takes the conversation from the agent.  ### Interactive replies  Button and list taps, flow responses and orders arrive under `metadata` (`interactiveType`, `interactiveId`, `flowResponseData`, `order`). Only a referral that arrives without a message becomes `referral.received`.  ### Platform notes  New email from Google, Microsoft and IMAP mailboxes arrives as this event. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_message** | [**WebhookPayloadMessage**](WebhookPayloadMessage.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_message_sent

> on_message_sent(webhook_payload_message_sent)
Message sent event

A message was sent through the API, the dashboard, or the WhatsApp Business app on Coexistence numbers.  ### Sender  `message.sentVia` is one of `human`, `api`, `broadcast`, `sequence`, `workflow`, `comment_automation` or `bulk-api`. It is `null` for sends from the platform's own app and for older messages; treat `null` as unknown, never as human.  ### Attribution keys  `automationId`, `workflowId`, `executionId`, `broadcastId` and `sequenceId` are always present. Each is `null` unless that kind of sender produced the message.  ### Quote replies  A quote-reply sent through the API carries `metadata.quotedMessageId`. One sent from the WhatsApp Business or Instagram app does not.  ### Platform notes  On Instagram and Facebook the attribution can be missing when Meta's echo of a send reaches Zernio before the send is recorded. On WhatsApp, Meta Business Agent replies carry `source: \"meta_business_agent\"`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_message_sent** | [**WebhookPayloadMessageSent**](WebhookPayloadMessageSent.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_notification_sent

> on_notification_sent(webhook_payload_notification_sent)
Notification sent event

Built for agents. One event for every notification we would email the account owner: a scheduled post failed to publish (`type: post_failed`), or a connected account was disconnected (`type: account_disconnected`).  It carries the email's `subject` and `text`, references to the post or account, and the `actions` that resolve it, so an agent subscribes to one event and handles every notification the same way.  ### Agents or state sync  Subscribe to `notification.sent` when an agent or automation reads the alert and acts on it. Subscribe to `post.platform.failed`, `post.failed`, `post.partial` and `account.disconnected` when your system keeps post and account state in sync: they carry the structured post or account and fire on every state change.  ### When it fires  Once for each such notification, in near real time, regardless of the user's email toggles, and even when the owner has no email address or the email is held back by the sender's limits. It fires alongside `post.failed` and `account.disconnected`, which stay as they are.  The user's notification channel (Slack or Telegram) follows the email toggles, so it only receives the alerts whose toggle is on.  - `post_failed`: once the failure is final (a permanent error, or a temporary one on its last retry), once per publish attempt that failed, for scheduled posts only (not \"post now\"). `refs.platforms` lists every platform that failed in that attempt. - `account_disconnected`: every time an account is disconnected, never for creator-profile accounts. `reason` says why.  ### Payload notes  `text` is the email body without the greeting. When your content retention is set to keep no content, the post text is replaced by `Content not retained` and each platform error by a generic description of its category.  ### How to act  Each entry of `actions` is a public API call with the ids already in the path: `retry_post` (`retryPost`, `POST /v1/posts/{postId}/retry`), `reconnect_account` (`getConnectUrl`, `GET /v1/connect/{platform}`) and `check_account` (`getAccountHealth`, `GET /v1/accounts/{accountId}/health`).  ### Who receives it  Endpoints subscribed to `notification.sent`. Scoped endpoints receive it for their profiles and accounts. Restricted keys need the `publishing` resource group. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_notification_sent** | [**WebhookPayloadNotificationSent**](WebhookPayloadNotificationSent.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_phone_number_stock_available

> on_phone_number_stock_available(webhook_payload_phone_number_stock_available)
Phone-number stock available event

A country you watch has deliverable phone numbers again; fires once per watch.  ### When it fires  Fired by the 6-hourly stock sweep, before you own a number in that country. The watch (`POST /v1/phone-numbers/stock-watches`) is then consumed.  ### Payload notes  `stock.country` is the watched country. `stock.types[]` lists each number type in stock with its `availableCount` at sweep time. Numbers are first come, first served; buy with `POST /v1/phone-numbers/purchase`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_phone_number_stock_available** | [**WebhookPayloadPhoneNumberStockAvailable**](WebhookPayloadPhoneNumberStockAvailable.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_authenticity_changed

> on_post_authenticity_changed(webhook_payload_post_authenticity_changed)
Post authenticity changed event

A tracked post's authenticity score crossed 40, in either direction.  ### When it fires  Only while the tracking window is open. A post's first score never fires it.  ### Payload notes  Carries `score`, `previousScore`, `confidence` and `reasons`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post_authenticity_changed** | [**WebhookPayloadPostAuthenticityChanged**](WebhookPayloadPostAuthenticityChanged.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_cancelled

> on_post_cancelled(webhook_payload_post)
Post cancelled event

A scheduled post was cancelled because its account was disconnected, and nothing published.  ### When it fires  A multi-platform post fires it only once every platform entry is cancelled. If a platform already published, the rollup is `post.partial` instead.  ### When it does not fire  `DELETE /v1/posts/{postId}` removes the post without sending this event. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post** | [**WebhookPayloadPost**](WebhookPayloadPost.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_external_created

> on_post_external_created(webhook_payload_external_post)
External post created event

A post authored natively on the platform, outside Zernio, was detected for the first time.  ### When it fires  Detected by a background sync roughly hourly, not in real time. Example: a Google Business Profile post created in the Google interface.  ### Payload notes  `post.source` is always `\"external\"` and `post.id` is the platform-native post id.  ### First sync backfill  On a freshly connected account, every existing native post fires it once. Treat it as an idempotent upsert keyed on `post.id`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_external_post** | [**WebhookPayloadExternalPost**](WebhookPayloadExternalPost.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_external_deleted

> on_post_external_deleted(webhook_payload_external_post)
External post deleted event

A tracked native post was removed from the platform.  ### Payload notes  `post.deletedAt` is the detection time.  ### Detection limits  Coverage is bounded to the most recent posts the platform listing returns, so very old deletions may go undetected.  ### When it does not fire  Detection diffs against posts a prior sync already indexed. An account with no indexed post never emits it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_external_post** | [**WebhookPayloadExternalPost**](WebhookPayloadExternalPost.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_external_updated

> on_post_external_updated(webhook_payload_external_post)
External post updated event

A tracked native post's text or media changed on the platform.  ### How edits are detected  Zernio compares text and media structure and, where available, the platform's own edit timestamp. A media-URL-only refresh (rotated CDN URLs) does not fire it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_external_post** | [**WebhookPayloadExternalPost**](WebhookPayloadExternalPost.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_failed

> on_post_failed(webhook_payload_post)
Post failed event

A post failed on every target platform.  ### When it fires  Once per publishing job, after every platform target ends. Exactly one of `post.published`, `post.partial` or `post.failed` fires.  A TikTok target TikTok is still processing (status `uploading`) holds it for up to 48 hours. Meanwhile `post.platform.published` and `post.platform.failed` report the other targets.  ### Payload notes  Each `platforms[]` entry carries `error`, `errorCategory` and `errorSource`, the same taxonomy as `platforms[]` on Get post. Branch on `errorCategory`, not on the message text. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post** | [**WebhookPayloadPost**](WebhookPayloadPost.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_partial

> on_post_partial(webhook_payload_post)
Post partial event

A post published on some platforms and failed on others.  ### When it fires  Once per publishing job, after every platform target ends. Exactly one of `post.published`, `post.partial` or `post.failed` fires.  A TikTok target TikTok is still processing (status `uploading`) holds it for up to 48 hours. Meanwhile `post.platform.published` and `post.platform.failed` report the other targets.  It can follow a `post.failed` for the same post when TikTok later reports a failed TikTok target as published.  ### Payload notes  Read `platforms[].status` to tell them apart. Failed entries carry `error`, `errorCategory` and `errorSource`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post** | [**WebhookPayloadPost**](WebhookPayloadPost.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_platform_deleted

> on_post_platform_deleted(webhook_payload_post_platform)
Post platform deleted event

A published platform target was deleted on the platform.  ### When it fires  Detected by a background sync roughly hourly, once per platform target. Platforms push no deletion notice, so it can trail the rollup by days.  ### Payload notes  `platform.status` is `deleted`. `platform.deletedAt` is the detection time, not the moment of deletion.  ### Detection limits  Detection is listing-based: coverage is bounded to the posts the listing returns, and rare false positives happen. The event is not retracted when the post reappears. Re-check before deleting.  ### When it does not fire  Detection diffs against posts a prior sync already indexed. An account with no indexed post never emits it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post_platform** | [**WebhookPayloadPostPlatform**](WebhookPayloadPostPlatform.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_platform_failed

> on_post_platform_failed(webhook_payload_post_platform)
Post platform failed event

One platform target failed permanently.  ### When it fires  Only on permanent failure; retryable errors stay silent. The rollup (`post.failed` or `post.partial`) fires separately once every platform ends.  ### After a publish  It can fire for a target that already emitted `post.platform.published`, if background reconciliation finds the publish never completed.  ### Payload notes  `platform.error` carries the platform's message. `platform.errorCategory` and `platform.errorSource` classify it, so a reconnect (`auth_expired`) separates from a content fix (`user_content`). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post_platform** | [**WebhookPayloadPostPlatform**](WebhookPayloadPostPlatform.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_platform_published

> on_post_platform_published(webhook_payload_post_platform)
Post platform published event

One platform target finished publishing, without waiting for the other targets.  ### When it fires  Once per platform target, as soon as it finishes. A cross-post to 2 accounts on the same platform produces 2 events. Use `post.published` for the post-level rollup.  ### Payload notes  `platform` carries the platform post id and URL. `account` identifies the connected account.  ### TikTok targets still processing  TikTok can keep processing a post for up to 48 hours (entry status `uploading`). That target fires when TikTok finishes. The other targets fire as they finish, and the post rollup waits for TikTok.  ### Later reconciliation  If a target later fails background reconciliation, `post.platform.failed` fires for the same target afterward.  A failed TikTok target that TikTok later reports as published fires `post.platform.published` afterward, and the rollup fires again. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post_platform** | [**WebhookPayloadPostPlatform**](WebhookPayloadPostPlatform.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_published

> on_post_published(webhook_payload_post)
Post published event

Every platform target of a post published.  ### When it fires  Once per publishing job, after every platform target ends. Exactly one of `post.published`, `post.partial` or `post.failed` fires.  A TikTok target TikTok is still processing (status `uploading`) holds it for up to 48 hours. Meanwhile `post.platform.published` and `post.platform.failed` report the other targets.  It can follow a `post.partial` or `post.failed` for the same post when TikTok later reports a failed TikTok target as published.  ### Payload notes  Each `platforms[]` entry carries the `platformPostId` and `publishedUrl`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post** | [**WebhookPayloadPost**](WebhookPayloadPost.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_recycled

> on_post_recycled(webhook_payload_post)
Post recycled event

A recycling schedule cloned a published post for republishing.  ### Payload notes  `post.id` is the new clone's id. The clone emits its own `post.scheduled`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post** | [**WebhookPayloadPost**](WebhookPayloadPost.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_scheduled

> on_post_scheduled(webhook_payload_post)
Post scheduled event

A post entered the scheduled state.  ### When it fires  Created with a schedule (with `publishNow`, accepted and queued), promoted from draft, added to a queue, retried after failing, or created as a recycled clone.  ### Approval and repeats  A post saved with `requiresApproval: true` fires it on approval, not at creation. One post can emit it more than once.  ### When it does not fire  Editing or moving an already-scheduled post to another time does not fire it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post** | [**WebhookPayloadPost**](WebhookPayloadPost.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_tik_tok_url_resolved

> on_post_tik_tok_url_resolved(webhook_payload_post_platform)
TikTok post URL resolved event

A published TikTok post's public URL became available.  ### When it fires  TikTok exposes the video id asynchronously, often minutes after upload, so `post.published` can carry an empty `publishedUrl`. Fires at most once per platform target. For a draft, it fires when the creator posts the draft publicly from the TikTok app.  ### Payload notes  Delivers `platform.publishedUrl` and the resolved `platform.platformPostId`. Same shape as `post.platform.published`.  ### When it does not fire  Private posts, which have no public URL, and drafts the creator never posts. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post_platform** | [**WebhookPayloadPostPlatform**](WebhookPayloadPostPlatform.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_post_tracking_completed

> on_post_tracking_completed(webhook_payload_post_tracking_completed)
Post tracking completed event

A post's tracking window ended and its final analytics read finished.  ### When it fires  Once per window. A cancelled window never fires it.  ### Payload notes  `final` holds the closing metrics, or is null when no sample could be read. When the post was deleted, it is the last sample held, if any.  ### Completion reasons  `window.completionReason` is `final_read` (the read succeeded), `unreachable` (the sync failed or no sample exists) or `post_deleted` (the post is gone). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_post_tracking_completed** | [**WebhookPayloadPostTrackingCompleted**](WebhookPayloadPostTrackingCompleted.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_rcs_agent_status_updated

> on_rcs_agent_status_updated(on_rcs_agent_status_updated_request)
RCS agent status updated event

An RCS agent moved into a new customer-visible status; `status` is the new one.  ### Statuses  `changes_requested` (note in `reason`), `brand_vetting`, `agent_review`, `testing`, `launch_review`, `launching`, `live`, `rejected` (`reason` says why), `deactivated`. In `testing`, add test phones, then file the launch; a `reason` means it bounced.  ### When it fires  Fires once per move into a status. `requested` sends nothing. Overlapping status checks never send the same status twice in a row.  ### Payload notes  `agent.profileId` is the owning profile. `agent.accountId` is `null` when the agent has no linked account. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_rcs_agent_status_updated_request** | [**OnRcsAgentStatusUpdatedRequest**](OnRcsAgentStatusUpdatedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_reaction_received

> on_reaction_received(webhook_payload_reaction)
Reaction received event

A participant added or removed an emoji reaction on a message on Instagram, Facebook, WhatsApp, Telegram, Slack or TikTok.  ### Payload notes  Sent as its own event, never as `message.received`. `reaction.action` is `added` or `removed`. `reaction.platformMessageId` is always present; `reaction.messageId` is the Zernio id when resolvable.  ### Removals  On WhatsApp, Instagram and Facebook removals, `reaction.emoji` is an empty string because the platform does not say which emoji went away. Match on `platformMessageId` to clear a mirrored reaction.  ### TikTok  A like or emoji reaction on a DM arrives only as this event, never as an empty `message.received`. `platformMessageId` is the TikTok id of the liked message. AI emoji reactions can have an empty `emoji`.  ### Telegram  The bot must be an administrator in the chat. Telegram does not send reactions in private chats to bots.  ### Accounts connected before August 2026  Instagram and Facebook accounts connected before August 2026 do not receive this event until their webhook subscription is refreshed. Reconnect them, or re-subscribe a Facebook Page without a reconnect. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_reaction** | [**WebhookPayloadReaction**](WebhookPayloadReaction.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_referral_received

> on_referral_received(webhook_payload_referral)
Referral received event

Someone opened an existing Instagram or Messenger thread through an ig.me or m.me `ref` link or returning ad click.  ### Payload notes  Meta's referral object is forwarded verbatim: `ref` and `source` for links, `ad_id` and `ads_context_data` for ad clicks.  ### When it does not fire  A referral that rides an inbound message arrives on `message.received` under `metadata.referral` instead. The two never fire for the same click.  ### Stored referral  The first referral captured on a conversation is also persisted on it (`metadata` on `GET /v1/inbox/conversations`). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_referral** | [**WebhookPayloadReferral**](WebhookPayloadReferral.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_review_deleted

> on_review_deleted(webhook_payload_review_deleted)
Review deleted event

Google Business Profile stopped returning a review, for example after its spam filter removed it.  ### When it fires  Zernio detects it by polling, so it usually fires 6 to 12 hours after the review disappears. Only locations covered by a webhook subscribed to `review.deleted` or `review.restored` are checked.  ### Restores  If the review comes back, `review.restored` fires, so a hidden then restored review produces `review.deleted` then `review.restored`. A `review.updated` can arrive for a deleted review; the next check restores it.  ### Payload notes  `review.id` is the full review name, the same value `review.new` sent. It may arrive for a review id you never received `review.new` for, so ignore ids you do not know. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_review_deleted** | [**WebhookPayloadReviewDeleted**](WebhookPayloadReviewDeleted.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_review_new

> on_review_new(webhook_payload_review_new)
Review new event

A new review was posted on a connected Google Business Profile account, in real time through Pub/Sub. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_review_new** | [**WebhookPayloadReviewNew**](WebhookPayloadReviewNew.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_review_restored

> on_review_restored(webhook_payload_review_restored)
Review restored event

Google returned a review previously reported by `review.deleted`; the payload has the same shape as `review.new`.  ### When it fires  It may reach a webhook that subscribed after the deletion, so ignore ids you do not know. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_review_restored** | [**WebhookPayloadReviewRestored**](WebhookPayloadReviewRestored.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_review_updated

> on_review_updated(webhook_payload_review_updated)
Review updated event

A Google Business Profile review changed: the reviewer edited it, or its reply was added, edited or removed.  ### Reply through the API  A reply sent through the Zernio API fires the event immediately. The periodic check then reports it again with the full review payload, so expect a second delivery.  ### Replies written in Google  Google sends no notification for replies written in its interface. The periodic check detects them, usually within 6 hours for reviews updated in the last 30 days, about 7 days for older.  ### Checks  Only teams with a webhook subscribed to `review.updated` are checked. A removed reply, through the API or in Google, fires from the periodic check with `review.hasReply` set to `false`.  ### Payload notes  Same shape as `review.new`. When a reply is present, `review.hasReply` is `true` and `review.reply` is populated. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_review_updated** | [**WebhookPayloadReviewUpdated**](WebhookPayloadReviewUpdated.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_sequence_enrolled

> on_sequence_enrolled(webhook_payload_sequence_enrollment)
Sequence enrolled event

A contact was enrolled in a sequence, through the API or a workflow `enroll_sequence` node. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_sequence_enrollment** | [**WebhookPayloadSequenceEnrollment**](WebhookPayloadSequenceEnrollment.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_sequence_exited

> on_sequence_exited(webhook_payload_sequence_enrollment)
Sequence exited event

A contact left a sequence; `exitReason` says why.  ### Exit reasons  - `completed`: the last step was sent. - `replied` - `manual`: unenrolled through the API. - `failed`: the step kept failing to send. - `unsubscribed` 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_sequence_enrollment** | [**WebhookPayloadSequenceEnrollment**](WebhookPayloadSequenceEnrollment.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_sms_registration_action_required

> on_sms_registration_action_required(on_sms_registration_action_required_request)
SMS registration action required event

An SMS registration is waiting on its owner; `reason` says why.  ### Reasons  - `changes_requested`: answer `message` via `POST /v1/sms/registrations/{id}/respond`. - `otp_required`: submit the texted code via `POST /v1/sms/registrations/{id}/verify-otp`; no `message`. - `carrier_info_required`: expires after 7 days.  ### When it fires  Fires once per new request and once per OTP or carrier request, not on follow-up messages. A carrier rejection alone does not fire it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_sms_registration_action_required_request** | [**OnSmsRegistrationActionRequiredRequest**](OnSmsRegistrationActionRequiredRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_sms_registration_status_updated

> on_sms_registration_status_updated(on_sms_registration_status_updated_request)
SMS registration status updated event

An SMS registration changed status; `status` is the new one.  ### Statuses  - `changes_requested`: answers needed. - `requested`: submitted, resubmitted, or your answers are back in review. - `pending`: with the carriers. - `approved`: live, attach numbers. - `rejected`: `reason` is the carriers' words. - `deactivated`  ### Rejections  A carrier rejection needs nothing from you. Zernio handles the fix and resends it, so the status returns to `pending`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_sms_registration_status_updated_request** | [**OnSmsRegistrationStatusUpdatedRequest**](OnSmsRegistrationStatusUpdatedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_support_run_completed

> on_support_run_completed(webhook_payload_support_run)
Support Assistant finished event

A support run finished with an answer, or handed the question to a person.  ### Payload notes  `run.status` is `completed`, or `needs_human` when Ana handed the question to a person. `run.answer` holds the answer; `run.stopReason` says why it stopped (`answered` or `human_review`, among others). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_support_run** | [**WebhookPayloadSupportRun**](WebhookPayloadSupportRun.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_support_run_failed

> on_support_run_failed(webhook_payload_support_run)
Support Assistant failed event

A support run failed or expired, and is not billed.  ### Payload notes  `run.status` is `failed` and `run.answer` is `null`. `run.stopReason` is `expired` when the run never finished. `run.costUsd` is 0. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_support_run** | [**WebhookPayloadSupportRun**](WebhookPayloadSupportRun.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_verification_approved

> on_verification_approved(on_verification_approved_request)
Verification approved event

The recipient submitted the right verification code.  ### Payload notes  Carries `verification.verificationId`, `verification.channel` (`sms`) and `verification.to`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_verification_approved_request** | [**OnVerificationApprovedRequest**](OnVerificationApprovedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_verification_failed

> on_verification_failed(on_verification_failed_request)
Verification failed event

A verification ran out of attempts without a correct code.  ### Payload notes  `reason` is `max_attempts_reached`. Carries the same `verification` fields as `verification.approved`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_verification_failed_request** | [**OnVerificationFailedRequest**](OnVerificationFailedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_webhook_test

> on_webhook_test(webhook_payload_test)
Webhook test event

Zernio sent a test event to an endpoint.  ### When it fires  Sent when you call Test webhook or press test in the dashboard, whatever events the endpoint subscribes to. Sent once, synchronously, and never retried. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_test** | [**WebhookPayloadTest**](WebhookPayloadTest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_account_alert_received

> on_whats_app_account_alert_received(webhook_payload_whats_app_account_alert_received)
WhatsApp account alert received

Meta sent an account alert for a connected WhatsApp Business Account.  ### Payload notes  Forwards Meta's `account_alerts` as is. `alert.severity` is `CRITICAL`, `WARNING` or `INFORMATIONAL`; `alert.type` is Meta's alert type; `alert.description` is the text.  ### Who receives it  An alert about one number goes to that number's account. A business-level alert goes to every connected number on the WABA. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_whats_app_account_alert_received** | [**WebhookPayloadWhatsAppAccountAlertReceived**](WebhookPayloadWhatsAppAccountAlertReceived.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_account_name_status_updated

> on_whats_app_account_name_status_updated(webhook_payload_whats_app_account_name_status_updated)
WhatsApp display-name review outcome event

Meta finished reviewing a WhatsApp display-name change on a connected number.  ### When it fires  Fires only on a review outcome, forwarded from Meta's `phone_number_name_update` field. A name applied without review (`AVAILABLE_WITHOUT_REVIEW`) produces no event.  ### Payload notes  Branch on `name.status` (`APPROVED`, `DECLINED`, `PENDING_REVIEW`). Meta's `REJECTED` maps to `DECLINED` and `DEFERRED` to `PENDING_REVIEW`, because the review is still open. `name.requestedName` and `name.rejectionReason` are Meta's values or null.  ### Delivery  Delivery is at-least-once; dedupe on `(account.accountId, name.status, name.requestedName)`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_whats_app_account_name_status_updated** | [**WebhookPayloadWhatsAppAccountNameStatusUpdated**](WebhookPayloadWhatsAppAccountNameStatusUpdated.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_account_quality_updated

> on_whats_app_account_quality_updated(webhook_payload_whats_app_account_quality_updated)
WhatsApp quality rating or messaging limit changed

A connected number's quality rating or messaging limit tier changed.  ### When it fires  Fires only when the rating or tier differs from the value Zernio held. A tier change Meta applies to the whole business portfolio fires once per connected number.  ### Payload notes  `quality.source` says which Meta signal reported it. Compare `quality.previousQualityRating` with `quality.qualityRating`, and the previous and current messaging limit tier. `quality.qualityRating` is Meta's live value (`GREEN`, `YELLOW`, `RED`).  ### Delivery  Delivery is at-least-once; dedupe on the event `id`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_whats_app_account_quality_updated** | [**WebhookPayloadWhatsAppAccountQualityUpdated**](WebhookPayloadWhatsAppAccountQualityUpdated.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_account_status_updated

> on_whats_app_account_status_updated(webhook_payload_whats_app_account_status_updated)
WhatsApp Business Account restricted or reinstated

Meta restricted, disabled, deleted or reinstated a connected WhatsApp Business Account, or flagged a violation on it.  ### When it fires  Mirrors Meta's `account_update` events. They apply to the whole WhatsApp Business Account, so every connected number on it receives one event.  ### Payload notes  Branch on `status.status` (`restricted` or `active`) and `status.metaEvent`. `status.restrictions` lists what Meta restricted (for example `RESTRICTED_BIZ_INITIATED_MESSAGING`) and when each lifts. The same status is on the account as `platformStatus`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_whats_app_account_status_updated** | [**WebhookPayloadWhatsAppAccountStatusUpdated**](WebhookPayloadWhatsAppAccountStatusUpdated.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_automatic_event

> on_whats_app_automatic_event(on_whats_app_automatic_event_request)
WhatsApp automatic event detected

Meta's automatic event identification detected a lead or purchase in a Click-to-WhatsApp conversation.  ### Payload notes  Branch on `eventName` (`LeadSubmitted` or `Purchase`). `Purchase` may carry the detected amount in `customData` (`currency`, `value`). It carries the `ctwaClid`.  ### Conversions API match key  Meta omits the clid on a minority of referrals, most often WhatsApp Status placements; this event can supply it. Zernio writes it onto the conversation, so `POST /v1/whatsapp/conversions` becomes usable for it.  ### Availability  Detection is not available for EU, UK and JP businesses. Elsewhere the owner opts in during Embedded Signup. An endpoint subscribed on a number whose owner did not opt in receives nothing. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_whats_app_automatic_event_request** | [**OnWhatsAppAutomaticEventRequest**](OnWhatsAppAutomaticEventRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_contact_identity_changed

> on_whats_app_contact_identity_changed(webhook_payload_whats_app_contact_identity_changed)
WhatsApp contact identity changed event

A WhatsApp user changed phone number or Meta regenerated their business-scoped user id (BSUID).  ### When it fires  Fires when Meta reports the user under a new phone number (`reason: \"user_changed_number\"`) or a new BSUID (`user_changed_user_id`, `user_identity_changed` or `user_id_update`).  ### Payload notes  `previous` and `current` carry the phone number, BSUID, parent BSUID and username. Use them to re-key records stored against the old value.  ### Already applied  Zernio has already moved the inbox conversation and the contact when the event arrives. `conversationId` and `contactId` point at them, or are null when there was none.  ### Delivery  Delivery is at-least-once; dedupe on the event `id`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_whats_app_contact_identity_changed** | [**WebhookPayloadWhatsAppContactIdentityChanged**](WebhookPayloadWhatsAppContactIdentityChanged.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_number_action_required

> on_whats_app_number_action_required(on_whats_app_number_action_required_request)
WhatsApp number action required event

The regulator asked for more information on a placed number order; nothing was rejected.  ### When it fires  The order stays pending, and the number stays `pending_regulatory`, until you provide the information. The status does not change.  ### Payload notes  `reason` carries the regulator's request verbatim when available. `requirements` lists every requirement with the reviewer's current verdict; the `declined` ones are what to fix, keyed by `requirementId`. Verdicts describe the review at `reviewedAt`.  ### How to resolve  Provide the missing details from the dashboard's phone-numbers page, or re-submit the fields through the remediation endpoint. The review resumes automatically. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_whats_app_number_action_required_request** | [**OnWhatsAppNumberActionRequiredRequest**](OnWhatsAppNumberActionRequiredRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_number_activated

> on_whats_app_number_activated(on_whats_app_number_activated_request)
WhatsApp number activated event

A number you provisioned through Zernio finished setup and is ready to connect.  ### When it fires  Regulated (non-US) numbers can take 1 to 3 business days after the order is approved. In instant-provisioning countries this is the first event, with no review states before it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_whats_app_number_activated_request** | [**OnWhatsAppNumberActivatedRequest**](OnWhatsAppNumberActivatedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_number_declined

> on_whats_app_number_declined(on_whats_app_number_declined_request)
WhatsApp number declined event

A regulated number order was declined in regulatory review and no number was activated.  ### Payload notes  `reason` carries the reviewer's rejection reason when available. You are never billed for a declined number.  ### Remediation  Resubmit corrected details and the number returns to `pending_regulatory`. It is the same number, with no new billing. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_whats_app_number_declined_request** | [**OnWhatsAppNumberDeclinedRequest**](OnWhatsAppNumberDeclinedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_number_kyc_submitted

> on_whats_app_number_kyc_submitted(on_whats_app_number_kyc_submitted_request)
WhatsApp number KYC submitted event

An end customer completed a hosted KYC share link and the number entered regulatory review.  ### When it fires  Fires only for hosted share links (`POST /v1/phone-numbers/kyc/share`). When you submit KYC over the API, no event fires.  ### What follows  The number is `pending_regulatory` under your account. `whatsapp.number.activated` or `whatsapp.number.declined` follows once the provider rules on it. Update your own UI from this event instead of polling. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_whats_app_number_kyc_submitted_request** | [**OnWhatsAppNumberKycSubmittedRequest**](OnWhatsAppNumberKycSubmittedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_number_reactivated

> on_whats_app_number_reactivated(on_whats_app_number_reactivated_request)
WhatsApp number reactivated event

A suspended number was reactivated, for example after the payment recovered, and is usable again. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_whats_app_number_reactivated_request** | [**OnWhatsAppNumberReactivatedRequest**](OnWhatsAppNumberReactivatedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_number_released

> on_whats_app_number_released(on_whats_app_number_released_request)
WhatsApp number released event

A number was released and is no longer usable.  ### Payload notes  Released by you, a billing cleanup or an admin. `reason` is a value such as `user_requested` or `cleanup_suspended`. This is the only terminal status. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_whats_app_number_released_request** | [**OnWhatsAppNumberReleasedRequest**](OnWhatsAppNumberReleasedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_number_suspended

> on_whats_app_number_suspended(on_whats_app_number_suspended_request)
WhatsApp number suspended event

An active number was suspended, for example after a failed payment.  ### Payload notes  `reason` is a value such as `payment_failed` or `subscription_ended`. The number stops working until the issue is resolved, then `whatsapp.number.reactivated` follows.  ### When it does not recover  A suspension left unresolved ends in release. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_whats_app_number_suspended_request** | [**OnWhatsAppNumberSuspendedRequest**](OnWhatsAppNumberSuspendedRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_number_verification_required

> on_whats_app_number_verification_required(on_whats_app_number_verification_required_request)
WhatsApp number verification-required event

A regulated number requires the end user to complete an identity check.  ### Payload notes  `verificationUrl` is a one-time link to forward to the person whose ID is on file, for example for Australian mobile numbers. The order completes once they pass. The number stays `pending_regulatory`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**on_whats_app_number_verification_required_request** | [**OnWhatsAppNumberVerificationRequiredRequest**](OnWhatsAppNumberVerificationRequiredRequest.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_template_category_updated

> on_whats_app_template_category_updated(webhook_payload_whats_app_template_category_updated)
WhatsApp template category updated event

Meta reclassified a WhatsApp template's category, first as a 24-hour advance notice and again when applied.  ### When it fires  Sent with `template.changeType: \"scheduled\"` for Meta's 24-hour advance notice, and again with `\"applied\"` when the change takes effect.  ### Payload notes  `template.category` is always the category right now. Meta clears a custom delivery window when it recategorises a template, so read `message_send_ttl_seconds` back after an `applied` change.  ### Platform notes  Forwarded from Meta's `template_category_update` field. The category decides Meta's per-delivery rate and the delivery window the template can carry. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_whats_app_template_category_updated** | [**WebhookPayloadWhatsAppTemplateCategoryUpdated**](WebhookPayloadWhatsAppTemplateCategoryUpdated.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_whats_app_template_status_updated

> on_whats_app_template_status_updated(webhook_payload_whats_app_template_status_updated)
WhatsApp template status updated event

Meta finished reviewing or re-reviewing a WhatsApp Business template on a connected WABA.  ### Payload notes  Branch on `template.status` (`APPROVED`, `REJECTED`, `PENDING`, `PAUSED`, `DISABLED`, `IN_APPEAL`, `PENDING_DELETION`). `template.reason` is Meta's free-form reason or `\"NONE\"`.  ### Platform notes  Forwarded from Meta's `message_template_status_update` field. Meta includes neither the previous status nor the template's category. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_whats_app_template_status_updated** | [**WebhookPayloadWhatsAppTemplateStatusUpdated**](WebhookPayloadWhatsAppTemplateStatusUpdated.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_workflow_run_completed

> on_workflow_run_completed(webhook_payload_workflow_run)
Workflow run completed event

A workflow run ended, with `execution.status` `completed`, or `exited` when it ended on purpose before its last node.  ### Exits  An exit is a handoff, or a button that switched the contact to another workflow. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_workflow_run** | [**WebhookPayloadWorkflowRun**](WebhookPayloadWorkflowRun.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_workflow_run_failed

> on_workflow_run_failed(webhook_payload_workflow_run)
Workflow run failed event

A workflow run failed; `error` names the node that failed and why. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_workflow_run** | [**WebhookPayloadWorkflowRun**](WebhookPayloadWorkflowRun.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## on_workflow_run_started

> on_workflow_run_started(webhook_payload_workflow_run)
Workflow run started event

A workflow run started for a conversation; `trigger.type` is the trigger node's type.  ### Payload notes  `trigger.text` is the inbound message that started the run, when there was one. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**webhook_payload_workflow_run** | [**WebhookPayloadWorkflowRun**](WebhookPayloadWorkflowRun.md) |  | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

