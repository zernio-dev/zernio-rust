# CreatePhoneNumberPortInRequestEndUser

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**entity_name** | **String** | Account holder / business name, as on the carrier account. | 
**auth_person_name** | **String** | Full name (first + last) of the person authorizing the port — must match the LOA signature. | 
**billing_phone_number** | Option<**String**> | Phone number on the losing carrier's bill. Defaults to the ported number itself on single-number orders. Validated as a real phone number when present. | [optional]
**account_number** | **String** | Account number with the losing carrier — required (carriers reject ports without it; on prepaid mobile plans it is often the phone number itself). | 
**pin_passcode** | Option<**String**> | Transfer PIN. Required for mobile numbers (wireless carriers reject PIN-less ports). Forwarded to the carrier, never stored. | [optional]
**street_address** | **String** |  | 
**extended_address** | Option<**String**> |  | [optional]
**locality** | **String** |  | 
**administrative_area** | **String** | 2-letter US state / CA province code (full names are accepted and normalized). | 
**postal_code** | **String** | US ZIP (5 digits) or Canadian postal code, matching countryCode. | 
**country_code** | **CountryCode** |  (enum: US, CA) | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


