# WebhookPayloadNotificationSentNotification

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**category** | **Category** | The email notification preference this notification belongs to. securityAlerts has no preference: it is always sent. (enum: postFailures, accountIssues, securityAlerts) | 
**r#type** | **Type** |  (enum: post_failed, account_disconnected, api_key_handed_over) | 
**subject** | **String** | The email subject. | 
**text** | **String** | The email body as plain text, without the greeting. | 
**url** | **String** | Dashboard link for the notification. | 
**refs** | [**models::WebhookPayloadNotificationSentNotificationRefs**](WebhookPayloadNotificationSentNotificationRefs.md) |  | 
**reason** | Option<**String**> | Why the account was disconnected. Only on account_disconnected. | [optional]
**actions** | [**Vec<models::WebhookPayloadNotificationSentNotificationActionsInner>**](WebhookPayloadNotificationSentNotificationActionsInner.md) | API calls that act on the notification, with the ids already in the path. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


