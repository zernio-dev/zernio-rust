# CheckPhoneNumberAvailability200ResponseAreaAvailability

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**in_stock** | Option<[**Vec<models::CheckPhoneNumberAvailability200ResponseAreaAvailabilityInStockInner>**](CheckPhoneNumberAvailability200ResponseAreaAvailabilityInStockInner.md)> | Deliverable numbers now, deepest first. Pass `ndc` as `areaCode` to hold the order to it. | [optional]
**pre_order** | Option<[**Vec<models::CheckPhoneNumberAvailability200ResponseAreaAvailabilityPreOrderInner>**](CheckPhoneNumberAvailability200ResponseAreaAvailabilityPreOrderInner.md)> | The carrier lists nothing there and the number type is a document tier: submit KYC with `areaCode` and `preOrder: true`, the carrier sources one (usually 2 to 4 weeks, never guaranteed), nothing is billed until it is active. | [optional]
**out_of_stock** | Option<[**Vec<models::CheckPhoneNumberAvailability200ResponseAreaAvailabilityOutOfStockInner>**](CheckPhoneNumberAvailability200ResponseAreaAvailabilityOutOfStockInner.md)> | Nothing deliverable and no pre-order: `listed` > 0 is stock the carrier shows that WhatsApp refused recently (held back until it clears), 0 is a dry area of an instant tier. A stock watch (POST /v1/phone-numbers/stock-watches with `areaCode`) is the way to hear when it is back. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


