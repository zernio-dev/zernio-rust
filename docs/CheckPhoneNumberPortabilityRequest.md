# CheckPhoneNumberPortabilityRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phone_numbers** | **Vec<String>** | E.164 numbers to check, e.g. +13035550000. At most one without an API key. | 
**claim_links** | Option<**bool**> | true adds `claimId` and `claimUrl` to portable results even when you send an API key, e.g. to hand a user a signup link that opens the port form with their number. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


