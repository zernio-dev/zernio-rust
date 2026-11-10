# CreateMicrosoftOrgConnectionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**scopes** | **Vec<Scopes>** |  (enum: email, calendar, files, contacts) | 
**allowed_emails** | Option<**Vec<String>**> | Addresses or `@domain` entries mailboxes must match. Omit for every mailbox. | [optional]
**redirect_url** | Option<**String**> | Where Microsoft sends the administrator after consent. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


