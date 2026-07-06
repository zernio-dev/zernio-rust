# StartSmsRegistrationRequestBrand

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**entity_type** | **EntityType** |  (enum: PRIVATE_PROFIT, PUBLIC_PROFIT, NON_PROFIT, GOVERNMENT, SOLE_PROPRIETOR) | 
**display_name** | **String** |  | 
**company_name** | Option<**String**> | Legal company name. Required for every entityType except SOLE_PROPRIETOR. | [optional]
**ein** | Option<**String**> | Required for every entityType except SOLE_PROPRIETOR. | [optional]
**phone** | Option<**String**> |  | [optional]
**mobile_phone** | Option<**String**> | Required for SOLE_PROPRIETOR; the verification OTP is texted there (US/CA mobile). | [optional]
**street** | Option<**String**> |  | [optional]
**city** | Option<**String**> |  | [optional]
**state** | Option<**String**> |  | [optional]
**postal_code** | Option<**String**> |  | [optional]
**country** | **Country** |  (enum: US, CA) | 
**email** | Option<**String**> | Brand contact email; defaults to your account email when omitted. | [optional]
**website** | Option<**String**> |  | [optional]
**vertical** | **Vertical** |  (enum: AGRICULTURE, COMMUNICATION, CONSTRUCTION, EDUCATION, ENERGY, ENTERTAINMENT, FINANCIAL, GAMBLING, GOVERNMENT, HEALTHCARE, HOSPITALITY, HUMAN_RESOURCES, INSURANCE, LEGAL, MANUFACTURING, NGO, POLITICAL, POSTAL, PROFESSIONAL, REAL_ESTATE, RETAIL, TECHNOLOGY, TRANSPORTATION) | 
**stock_symbol** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


