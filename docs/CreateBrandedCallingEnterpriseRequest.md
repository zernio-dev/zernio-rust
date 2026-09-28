# CreateBrandedCallingEnterpriseRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**legal_name** | **String** | Exactly as on the tax record. | 
**doing_business_as** | **String** |  | 
**organization_type** | **OrganizationType** |  (enum: commercial, government, non_profit) | 
**organization_legal_type** | **OrganizationLegalType** |  (enum: corporation, llc, partnership, nonprofit, other) | 
**country_code** | **String** | ISO 3166-1 alpha-2. US or CA. | 
**jurisdiction_of_incorporation** | **String** | State, province or country of registration. | 
**website** | **String** |  | 
**fein** | **String** | US Federal Employer Identification Number (NN-NNNNNNN) or the Canadian equivalent. Stored encrypted; only the last four digits are ever returned. | 
**industry** | **String** | One of the carrier industry labels, e.g. technology, healthcare, retail, finance, legal, insurance, real estate, logistics, education. | 
**number_of_employees** | **NumberOfEmployees** |  (enum: 1-10, 11-50, 51-200, 201-500, 501-2000, 2001-10000, 10001+) | 
**organization_contact** | [**models::BrandedCallingContact**](BrandedCallingContact.md) |  | 
**billing_contact** | [**models::BrandedCallingContact**](BrandedCallingContact.md) |  | 
**physical_address** | [**models::BrandedCallingAddress**](BrandedCallingAddress.md) |  | 
**billing_address** | [**models::BrandedCallingAddress**](BrandedCallingAddress.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


