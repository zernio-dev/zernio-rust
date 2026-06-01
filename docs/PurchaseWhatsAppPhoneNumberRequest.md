# PurchaseWhatsAppPhoneNumberRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** | Profile to associate the number with | 
**country** | Option<**String**> | ISO 3166-1 alpha-2 country for the number (default US). International numbers require usage-based billing. Tier 3/4 countries return 202 { status: \"kyc_required\", kycUrl } — the customer must complete KYC at that URL before the number is ordered. See GET /v1/whatsapp/phone-numbers/countries.  | [optional][default to US]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


