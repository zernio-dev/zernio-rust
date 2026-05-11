# UpdateTrackingTagRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**enable_automatic_matching** | Option<**bool**> | Meta Advanced Matching toggle (`enable_automatic_matching`). | [optional]
**automatic_matching_fields** | Option<**Vec<AutomaticMatchingFields>**> | Which user fields Advanced Matching may collect. Meta's terse codes: em=email, ph=phone, fn=first name, ln=last name, ge=gender, db=date of birth, ct=city, st=state, zp=zip.  (enum: em, ph, fn, ln, ge, db, ct, st, zp, country, external_id) | [optional]
**first_party_cookie_status** | Option<**FirstPartyCookieStatus**> |  (enum: empty, first_party_cookie_disabled, first_party_cookie_enabled) | [optional]
**data_use_setting** | Option<**DataUseSetting**> |  (enum: advertising_and_analytics, analytics_only, empty) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


