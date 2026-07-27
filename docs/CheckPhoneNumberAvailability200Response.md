# CheckPhoneNumberAvailability200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**country** | Option<**String**> |  | [optional]
**number_type** | Option<**String**> |  | [optional]
**available** | Option<**bool**> | Whether deliverable voice inventory exists right now. | [optional]
**address_constraint** | Option<**AddressConstraint**> |  (enum: geo, country, none) | [optional]
**areas** | Option<**Vec<String>**> | For `geo` only — the area(s) the registered address must be in. | [optional]
**area_options** | Option<[**Vec<models::CheckPhoneNumberAvailability200ResponseAreaOptionsInner>**](CheckPhoneNumberAvailability200ResponseAreaOptionsInner.md)> | Live inventory grouped by area code. For US and CA this is the full country inventory (every area code with stock, recognizable metros listed first, then alphabetical); other countries are ordered largest stock first; they list the areas in the latest inventory page (up to 500 numbers, which for most countries is the entire pool). Empty when out of stock (or the area lookup failed). Pass a chosen `ndc` as `areaCode` on POST /v1/phone-numbers/purchase (or on the KYC submit for regulated countries) to require that area.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


