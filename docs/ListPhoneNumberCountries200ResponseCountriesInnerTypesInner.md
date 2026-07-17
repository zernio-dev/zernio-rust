# ListPhoneNumberCountries200ResponseCountriesInnerTypesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**number_type** | Option<**NumberType**> |  (enum: local, mobile, national, toll_free) | [optional]
**tier** | Option<**Tier**> |  (enum: 1, 2, 3, 4) | [optional]
**needs_kyc** | Option<**bool**> |  | [optional]
**monthly_cents** | Option<**i32**> |  | [optional]
**whatsapp_available** | Option<**bool**> | Always false for toll_free (WhatsApp does not reliably register toll-free numbers). | [optional]
**sms_available** | Option<**bool**> |  | [optional]
**calls_available** | Option<**bool**> |  | [optional]
**in_stock** | Option<**bool**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


