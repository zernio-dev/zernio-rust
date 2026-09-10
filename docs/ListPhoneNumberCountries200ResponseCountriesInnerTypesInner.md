# ListPhoneNumberCountries200ResponseCountriesInnerTypesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**number_type** | Option<**NumberType**> |  (enum: local, mobile, national, toll_free) | [optional]
**tier** | Option<**Tier**> | Null on a `fulfilment: request` type, whose document tier is only known once its requirements are read. (enum: 1, 2, 3, 4, ) | [optional]
**needs_kyc** | Option<**bool**> |  | [optional]
**monthly_cents** | Option<**i32**> | Price a NEW number of this type costs per month, in cents. | [optional]
**whatsapp_available** | Option<**bool**> | Always false for toll_free (WhatsApp does not reliably register toll-free numbers). | [optional]
**sms_available** | Option<**bool**> |  | [optional]
**calls_available** | Option<**bool**> |  | [optional]
**in_stock** | Option<**bool**> |  | [optional]
**fulfilment** | Option<**Fulfilment**> | `request`: the carrier stocks this type nowhere and only sources it to order, so it is always a pre-order. (enum: instant, request) | [optional]
**pre_orderable** | Option<**bool**> | Out of stock but orderable anyway. Submit KYC as usual (POST /v1/phone-numbers/kyc): we buy regular stock the moment it returns, otherwise the carrier sources the number. Usually 2 to 4 weeks, never guaranteed. Only document tiers (3/4) qualify, and nothing is billed until the number is active. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


