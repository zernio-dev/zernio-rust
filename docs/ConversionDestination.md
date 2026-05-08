# ConversionDestination

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Platform-native identifier. Pass back as `destinationId` on event send and as the path segment on CRUD endpoints.  | 
**name** | **String** |  | 
**r#type** | Option<**String**> | Present when the platform locks the event type/category to the destination (Google conversion actions, LinkedIn conversion rules). Absent for Meta pixels (which accept any event name per request).  | [optional]
**status** | Option<**Status**> | For LinkedIn, `inactive` means the rule is soft-deleted (`enabled: false`).  (enum: active, inactive) | [optional]
**ad_account_id** | Option<**String**> | Set by adapters whose destinations are scoped to a specific ad account (LinkedIn). Pass back on subsequent CRUD calls to identify the parent ad account.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


