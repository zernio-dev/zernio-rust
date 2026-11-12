# AutomationEventTrigger

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**r#type** | **Type** | The Zernio event that starts it. (enum: post.failed, post.partial, post.published, post.scheduled, post.recycled, post.platform.published, post.platform.failed, post.platform.deleted, post.external.created, account.connected, account.disconnected, account.permissions_changed, account.rate_limited, account.ads.sync_failed, ad.status_changed, ad.review.rejected, ad.delivery_issue, campaign.budget.depleted, ad_account.status_changed, campaign.status_changed, whatsapp.template.status_updated, whatsapp.account.quality_updated, commerce.order.created, commerce.order.updated, commerce.order.refunded, message.received, message.failed, conversation.started, reaction.received, referral.received, comment.received, review.new, call.received, call.ended, call.failed, lead.received) | 
**profile_id** | **String** | The profile whose events start it, from `GET /v1/profiles`. | 
**account_ids** | Option<**Vec<String>**> | Only events of these accounts. Leave out for every account of the profile. | [optional]
**filter** | Option<[**models::AutomationFactCondition**](AutomationFactCondition.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


