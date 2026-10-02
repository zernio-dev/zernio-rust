# SelectGoogleBusinessLocationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** | Profile ID from your connection flow | 
**location_id** | Option<**String**> | The Google Business Profile location ID selected by the user. Send this or locations, not both. | [optional]
**locations** | Option<[**Vec<models::SelectGoogleBusinessLocationRequestLocationsInner>**](SelectGoogleBusinessLocationRequestLocationsInner.md)> | Several locations to connect from one sign-in, each as its own account. The sign-in is used once for the whole batch and handed back only if none connected. With two or more distinct locations the response lists `accounts` and `failed` instead of `account`, and the request is refused with 400 on a reconnect. A single location behaves exactly like locationId. | [optional]
**account_id** | Option<**String**> | Optional but recommended. The Google Business Profile Account resource name (\"accounts/123\") that owns the selected location (returned per-location by GET /v1/connect/googlebusiness/locations). When provided, the location is resolved directly instead of by enumerating the account, which is required for accounts that own many locations. Omit only for small accounts.  | [optional]
**pending_data_token** | **String** | Token from the OAuth callback redirect (pendingDataToken query param). Tokens and profile data are retrieved server-side from this token. | 
**redirect_url** | Option<**String**> | Optional custom redirect URL to return to after selection | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


