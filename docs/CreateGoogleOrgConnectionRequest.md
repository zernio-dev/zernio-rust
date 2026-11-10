# CreateGoogleOrgConnectionRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**domain** | **String** | The Workspace domain the admin delegates. | 
**scopes** | **Vec<Scopes>** | Areas the mailboxes get, the same as a user connect. (enum: email, calendar, files, contacts) | 
**admin_email** | Option<**String**> | A super admin, used to list the domain's users. | [optional]
**allowed_emails** | Option<**Vec<String>**> | Addresses or `@domain` entries mailboxes must match. Omit for every mailbox. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


