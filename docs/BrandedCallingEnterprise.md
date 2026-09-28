# BrandedCallingEnterprise

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**legal_name** | Option<**String**> |  | [optional]
**doing_business_as** | Option<**String**> |  | [optional]
**organization_type** | Option<**OrganizationType**> |  (enum: commercial, government, non_profit) | [optional]
**organization_legal_type** | Option<**OrganizationLegalType**> |  (enum: corporation, llc, partnership, nonprofit, other) | [optional]
**country_code** | Option<**CountryCode**> |  (enum: US, CA) | [optional]
**jurisdiction_of_incorporation** | Option<**String**> |  | [optional]
**website** | Option<**String**> |  | [optional]
**fein_last4** | Option<**String**> | Last four digits of the tax id; the full id is never returned. | [optional]
**industry** | Option<**String**> |  | [optional]
**number_of_employees** | Option<**NumberOfEmployees**> |  (enum: 1-10, 11-50, 51-200, 201-500, 501-2000, 2001-10000, 10001+) | [optional]
**organization_contact** | Option<[**models::BrandedCallingContact**](BrandedCallingContact.md)> |  | [optional]
**billing_contact** | Option<[**models::BrandedCallingContact**](BrandedCallingContact.md)> |  | [optional]
**physical_address** | Option<[**models::BrandedCallingAddress**](BrandedCallingAddress.md)> |  | [optional]
**billing_address** | Option<[**models::BrandedCallingAddress**](BrandedCallingAddress.md)> |  | [optional]
**registered** | Option<**bool**> | True once the business exists at the carrier (happens when its first identity passes review). | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


