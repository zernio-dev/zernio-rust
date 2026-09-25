# SearchAvailablePhoneNumbers200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**country** | Option<**String**> |  | [optional]
**number_type** | Option<**String**> |  | [optional]
**require_sms** | Option<**bool**> | Echo of the `sms` filter applied to this search. | [optional]
**numbers** | Option<[**Vec<models::SearchAvailablePhoneNumbers200ResponseNumbersInner>**](SearchAvailablePhoneNumbers200ResponseNumbersInner.md)> |  | [optional]
**masked** | Option<**bool**> | true on keyless calls. | [optional]
**near** | Option<**String**> | With `country=auto`: the caller's city the results were narrowed to, or null when there was no stock there. | [optional]
**claim_id** | Option<**String**> | Keyless calls only: a claim for any number matching this search's country, type and area. | [optional]
**claim_url** | Option<**String**> | Keyless calls only: signup link for any number matching this search. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


