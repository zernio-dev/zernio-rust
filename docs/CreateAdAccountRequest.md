# CreateAdAccountRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio metaads SocialAccount ID. | 
**business_id** | **String** | Business portfolio that will own the account. | 
**name** | **String** | Ad account name. Whitespace is trimmed. | 
**currency** | **String** | Uppercase ISO 4217 currency supported by Meta. | 
**timezone_id** | **i32** | Numeric Meta timezone ID from the linked timezone list. For example 1 is America/Los_Angeles. | 
**end_advertiser** | Option<**String**> | End advertiser business or page ID. NONE uses the owning business. | [optional][default to NONE]
**media_agency** | Option<**String**> | Media agency business or page ID. NONE for self-serve customers. | [optional][default to NONE]
**partner** | Option<**String**> | Partner business or page ID. NONE for self-serve customers. | [optional][default to NONE]
**invoice** | Option<**bool**> | Request Meta invoicing. Eligibility is determined by Meta. | [optional]
**invoice_group_id** | Option<**String**> | Existing Meta invoice group ID. | [optional]
**invoicing_emails** | Option<**Vec<String>**> | Addresses for Meta invoices. | [optional]
**io** | Option<**bool**> | Meta insertion-order invoicing option. | [optional]
**po_number** | Option<**String**> | Purchase order number. | [optional]
**funding_id** | Option<**String**> | Existing Meta funding reference. Does not add a payment method. | [optional]
**ad_account_created_from_bm_flag** | Option<**bool**> | Meta Business Manager creation flag. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


