# SelectGoogleBusinessLocationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** | Profile ID from your connection flow | 
**location_id** | **String** | The Google Business location ID selected by the user | 
**account_id** | Option<**String**> | Optional but recommended. The Google Business Account resource name (\"accounts/123\") that owns the selected location (returned per-location by GET /v1/connect/googlebusiness/locations). When provided, the location is resolved directly instead of by enumerating the account, which is required for accounts that own many locations. Omit only for small accounts.  | [optional]
**pending_data_token** | **String** | Token from the OAuth callback redirect (pendingDataToken query param). Tokens and profile data are retrieved server-side from this token. | 
**redirect_url** | Option<**String**> | Optional custom redirect URL to return to after selection | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


