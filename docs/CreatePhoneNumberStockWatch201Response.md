# CreatePhoneNumberStockWatch201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** |  | 
**country** | **String** | ISO 3166-1 alpha-2. | 
**country_name** | **String** |  | 
**number_type** | Option<**NumberType**> | The watched number type, or null when the watch covers every type in the country. (enum: local, mobile, national, toll_free, ) | 
**area_code** | Option<**String**> | The watched area code (NDC), or null when the watch covers every area. | [optional]
**created_at** | **String** |  | 
**pre_orderable** | Option<**bool**> | True when the watched area can be bought today as a pre-order (the carrier lists nothing there and the type is a document tier): submit KYC with `areaCode` and `preOrder: true` instead of waiting, usually 2 to 4 weeks, nothing billed until active. The watch is armed either way. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


