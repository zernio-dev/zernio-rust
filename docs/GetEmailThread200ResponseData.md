# GetEmailThread200ResponseData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**provider** | Option<**Provider**> |  (enum: google, microsoft) | [optional]
**subject** | Option<**String**> |  | [optional]
**snippet** | Option<**String**> |  | [optional]
**participants** | Option<[**Vec<models::EmailAddress>**](EmailAddress.md)> |  | [optional]
**message_ids** | Option<**Vec<String>**> |  | [optional]
**draft_ids** | Option<**Vec<String>**> |  | [optional]
**folders** | Option<**Vec<String>**> |  | [optional]
**has_attachments** | Option<**bool**> |  | [optional]
**has_drafts** | Option<**bool**> |  | [optional]
**unread** | Option<**bool**> |  | [optional]
**starred** | Option<**bool**> |  | [optional]
**earliest_message_at** | Option<**String**> |  | [optional]
**latest_message_received_at** | Option<**String**> |  | [optional]
**latest_message_sent_at** | Option<**String**> |  | [optional]
**messages** | Option<[**Vec<models::EmailMessage>**](EmailMessage.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


