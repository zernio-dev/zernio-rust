# ListFormLeads200ResponseMeta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | Option<**String**> |  | [optional]
**account_id** | Option<**String**> |  | [optional]
**form_id** | Option<**String**> |  | [optional]
**source** | Option<**Source**> | persisted: leads stored from the webhook and the reconcile pass. live: read from Meta because none are stored for this form yet. (enum: persisted, live) | [optional]
**last_checked_at** | Option<**String**> | When Zernio last read this form's leads from Meta. For persisted leads, the last reconcile pass for the Page (null before the first one). For live reads, when the cached Graph read was made. | [optional]
**last_updated** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


