# BulkCreateContactsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** |  | 
**account_id** | Option<**String**> | Required when contacts carry channel data (platformIdentifier or a row-level accountId). Omit for a plain CRM import with no channels. | [optional]
**platform** | Option<**String**> | Ignored when accountId is set: the platform is derived from the resolved account. Only relevant to disambiguate accountId lookup; a mismatch 404s. | [optional]
**contacts** | [**Vec<models::BulkCreateContactsRequestContactsInner>**](BulkCreateContactsRequestContactsInner.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


