# GetPhoneNumberKycForm200ResponseReusableOptionsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Opaque option id — pass as `reuseOptionId` on POST. Stable selection key (a phone number is not unique across verifications). | [optional]
**from_phone_number** | Option<**String**> | Display only — the number this verification was submitted for. Not a selection key. | [optional]
**instant** | Option<**bool**> | true = group-approved, a new order activates in minutes; false = documents are reused but the order still queues for carrier review (1-3 days). | [optional]
**details** | Option<[**Vec<models::GetPhoneNumberKycForm200ResponseReusableOptionsInnerDetailsInner>**](GetPhoneNumberKycForm200ResponseReusableOptionsInnerDetailsInner.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


