# UpdateGmbLocationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**selected_location_id** | **String** |  | 
**google_account_id** | Option<**String**> | Optional but recommended. The Google Business Account resource name (\"accounts/123\") that owns the new location (from GET gmb-locations). When provided, the location is resolved directly instead of by enumerating the account, which is required for accounts with many locations. Named `googleAccountId` to disambiguate from the path `accountId` (the Zernio account). The legacy field name `accountId` is still accepted for backwards compatibility.  | [optional]
**account_id** | Option<**String**> | Legacy alias for googleAccountId. Use googleAccountId for new integrations. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


