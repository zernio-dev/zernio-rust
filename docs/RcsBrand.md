# RcsBrand

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**display_name** | **String** |  | 
**legal_name** | **String** | Exactly as on IRS records. | 
**legal_entity_type** | **LegalEntityType** |  (enum: LIMITED_LIABILITY_COMPANY, SOLE_PROPRIETORSHIP, PARTNERSHIP, CORPORATION, S_CORPORATION) | 
**organization_type** | **OrganizationType** |  (enum: PRIVATE_PROFIT, PUBLIC_PROFIT, NON_PROFIT, GOVERNMENT) | 
**website_url** | **String** |  | 
**tax_id** | **String** | US: the EIN, 9 digits, optionally NN-NNNNNNN. Elsewhere: the national tax or company registration id. | 
**stock_symbol** | Option<**String**> | EXCHANGE:SYMBOL. Required for PUBLIC_PROFIT. | [optional]
**address** | [**models::RcsBrandInputAddress**](RcsBrandInputAddress.md) |  | 
**contact** | [**models::RcsBrandInputContact**](RcsBrandInputContact.md) |  | 
**id** | Option<**String**> |  | [optional]
**status** | Option<**Status**> | draft = not filed yet (still editable). (enum: draft, vetting, verified, rejected) | [optional]
**created_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


