# SearchAvailablePhoneNumbers200ResponseNumbersInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phone_number** | Option<**String**> | E.164. Pass it as `phoneNumber` on POST /v1/phone-numbers/purchase to buy this exact number. | [optional]
**features** | Option<**Vec<String>**> | Provider capability list for this number (e.g. voice, sms, mms). | [optional]
**locality** | Option<**String**> | Town or rate center the number belongs to, as the carrier names it (e.g. WACO). | [optional]
**best_effort** | Option<**bool**> | true when the carrier added this number because too few matched your filters, so it may be outside the requested prefix or locality. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


