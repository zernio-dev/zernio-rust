# AssignGoogleBusinessLocationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** | Target profile to connect the location onto. | 
**selected_location_id** | **String** | The Google Business location ID to assign (e.g. \"locations/123\"). | 
**google_account_id** | Option<**String**> | Optional but recommended. The Google Business Account resource name (\"accounts/123\") that owns the location (from GET gmb-locations). When provided the location is resolved directly instead of by enumerating the account, required for accounts with many locations.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


