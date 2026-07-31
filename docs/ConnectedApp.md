# ConnectedApp

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**client_id** | Option<**String**> |  | [optional]
**client_name** | Option<**String**> | Name the client declared at registration. Registration is open, so this is self-declared and not verified. | [optional]
**redirect_host** | Option<**String**> | Host of the client's registered redirect URI (non-http schemes are shown as scheme//host). The destination an impostor cannot fake. | [optional]
**scopes** | Option<**Vec<String>**> | Scopes granted on the most recent token. | [optional]
**authorized_at** | Option<**String**> |  | [optional]
**last_used_at** | Option<**String**> | Last time any of the client's live tokens authenticated a request. | [optional]
**token_count** | Option<**i32**> | Live tokens held by the client (an active session is typically one access plus one refresh token). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


