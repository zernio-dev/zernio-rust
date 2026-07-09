# StartSmsRegistrationRequestBrand

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**entity_type** | **EntityType** |  (enum: PRIVATE_PROFIT, PUBLIC_PROFIT, NON_PROFIT, GOVERNMENT, SOLE_PROPRIETOR) | 
**display_name** | **String** |  | 
**company_name** | Option<**String**> | Legal company name. Required for every entityType except SOLE_PROPRIETOR. | [optional]
**ein** | Option<**String**> | Required for every entityType except SOLE_PROPRIETOR. | [optional]
**phone** | Option<**String**> | Business contact phone. Required for every entityType except SOLE_PROPRIETOR. | [optional]
**mobile_phone** | Option<**String**> | Required for SOLE_PROPRIETOR; the verification OTP is texted there (US/CA mobile). | [optional]
**street** | **String** |  | 
**city** | **String** |  | 
**state** | **String** |  | 
**postal_code** | **String** |  | 
**country** | **Country** |  (enum: US, CA) | 
**email** | Option<**String**> | Brand contact email; defaults to your account email when omitted. | [optional]
**website** | **String** | The brand's website (sole proprietors may use a social profile such as LinkedIn or a business Facebook page). Carriers verify the brand against it; a bare domain is normalized to https://. | 
**vertical** | **Vertical** |  (enum: AGRICULTURE, COMMUNICATION, CONSTRUCTION, EDUCATION, ENERGY, ENTERTAINMENT, FINANCIAL, GAMBLING, GOVERNMENT, HEALTHCARE, HOSPITALITY, HUMAN_RESOURCES, INSURANCE, LEGAL, MANUFACTURING, NGO, POLITICAL, POSTAL, PROFESSIONAL, REAL_ESTATE, RETAIL, TECHNOLOGY, TRANSPORTATION) | 
**stock_symbol** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


