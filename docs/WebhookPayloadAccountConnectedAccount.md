# WebhookPayloadAccountConnectedAccount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | The account's unique identifier (same as used in /v1/accounts/{accountId}) | 
**profile_id** | **String** | The profile's unique identifier this account belongs to | 
**platform** | **String** |  | 
**username** | **String** |  | 
**display_name** | Option<**String**> |  | [optional]
**reconnected** | Option<**bool**> | Present and true when a reconnect restored an existing account in place, keeping its accountId. | [optional]
**replaced_account_id** | Option<**String**> | The IMAP account this connection replaces, when a reconnected mailbox moved to Google or Microsoft. That account is retired at the same time, with account.disconnected and reasonCode replaced. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


