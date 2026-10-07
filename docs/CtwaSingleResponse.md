# CtwaSingleResponse

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_type** | **AdType** |  (enum: single) | 
**ad** | **serde_json::Value** | The persisted Ad document. | 
**message** | **String** |  | 
**warnings** | Option<**Vec<String>**> | Present when Meta created the ad set differently from the request. Today: Meta kept the ad set without the requested `whatsappPhoneNumber` in its promoted_object (the ads still carry it on their WhatsApp button). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


