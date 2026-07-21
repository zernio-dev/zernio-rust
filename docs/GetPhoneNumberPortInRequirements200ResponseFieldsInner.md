# GetPhoneNumberPortInRequirements200ResponseFieldsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**requirement_id** | Option<**String**> | Pass back as requirements[].requirementTypeId. | [optional]
**label** | Option<**String**> |  | [optional]
**kind** | Option<**Kind**> | text/date take a string value; file takes a documentId from the documents endpoint; address is satisfied automatically from the end-user service address. (enum: text, date, address, file, action) | [optional]
**description** | Option<**String**> |  | [optional]
**example** | Option<**String**> |  | [optional]
**acceptable_values** | Option<**Vec<String>**> | When present, the value must be one of these. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


