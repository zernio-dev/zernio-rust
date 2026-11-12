# SelectGoogleBusinessLocation200ResponseAccount

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | Option<**String**> | ID of the created SocialAccount | [optional]
**platform** | Option<**Platform**> |  (enum: googlebusiness) | [optional]
**username** | Option<**String**> |  | [optional]
**display_name** | Option<**String**> |  | [optional]
**is_active** | Option<**bool**> |  | [optional]
**selected_location_name** | Option<**String**> | Human-readable location display name, NOT a resource name. Do not use it to build API paths. Null when connected with no location. | [optional]
**selected_location_id** | Option<**String**> | Bare Google Business Profile location id. Combine with the Google Business Profile account id as accounts/{gbpAccountId}/locations/{selectedLocationId} to form the location resource names that gmb-reviews/batch expects in locationNames. Null when connected with no location. | [optional]
**needs_location** | Option<**bool**> | Present and true when the account was connected with no location (allowNoLocation=true). Create one with POST /v1/accounts/{accountId}/gmb-locations before using the location endpoints. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


