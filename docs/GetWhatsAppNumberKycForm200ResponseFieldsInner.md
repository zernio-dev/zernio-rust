# GetWhatsAppNumberKycForm200ResponseFieldsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**requirement_id** | Option<**String**> |  | [optional]
**label** | Option<**String**> |  | [optional]
**kind** | Option<**Kind**> | \"action\" = an out-of-band verification (e.g. Onfido); not filled here, fulfilled after the order via a link. (enum: text, date, address, file, action) | [optional]
**description** | Option<**String**> | Plain-English explanation of what to provide. | [optional]
**example** | Option<**String**> | Concrete example value. | [optional]
**local_to** | Option<**String**> | ISO country the value must be local to | [optional]
**audience** | Option<**Audience**> | When set, the requirement applies ONLY to this end-user type — provide it for that type and OMIT it for the other (e.g. Brazil: \"Cartão CNPJ\" is business-only, \"CPF\" and \"ID/Passport Copy\" are personal-only). Submitting both sets makes the regulator ask whether the number is for personal or business use and stalls the review. Pass `entityType` on POST so the server drops the inapplicable set. (enum: business, individual, ) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


