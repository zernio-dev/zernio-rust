# ListPhoneNumberCountries200ResponseCountriesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | Option<**String**> | ISO 3166-1 alpha-2 | [optional]
**tier** | Option<**Tier**> |  (enum: 1, 2, 3, 4) | [optional]
**monthly_cents** | Option<**i32**> |  | [optional]
**needs_kyc** | Option<**bool**> |  | [optional]
**calls_available** | Option<**bool**> | Regular phone (PSTN) calling on the number, inbound + outbound. Available on every offerable country. | [optional]
**whatsapp_available** | Option<**bool**> | WhatsApp can be enabled on numbers from this country. | [optional]
**sms_available** | Option<**bool**> | Whether this country's number type can do SMS. Use it to filter the picker when the buyer wants SMS (pair with `wantsSms` on purchase). | [optional]
**outbound_calling_available** | Option<**bool**> | WhatsApp Business Calling (BIC) outbound availability, a Meta feature blocked in some countries. NOT the PSTN Calls feature (`callsAvailable`). | [optional]
**in_stock** | Option<**bool**> | Live carrier-stock snapshot (refreshed every 6h + on availability checks): false when NO offered type currently has deliverable inventory, so a purchase would fail. Treat as advisory; the purchase itself re-checks. | [optional]
**types** | Option<[**Vec<models::ListPhoneNumberCountries200ResponseCountriesInnerTypesInner>**](ListPhoneNumberCountries200ResponseCountriesInnerTypesInner.md)> | Every number type offered in this country (default first). Capabilities, KYC tier, monthly price, and stock are per type. The country-level fields above mirror the first (default) entry. Pass the chosen `numberType` to POST /v1/phone-numbers/purchase.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


