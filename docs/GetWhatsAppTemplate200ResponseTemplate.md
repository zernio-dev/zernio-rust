# GetWhatsAppTemplate200ResponseTemplate

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Meta template id. Unique per language variant; usable on /v1/whatsapp/templates/id/{templateId}. | [optional]
**name** | Option<**String**> |  | [optional]
**status** | Option<**String**> |  | [optional]
**category** | Option<**String**> |  | [optional]
**language** | Option<**String**> | The variant actually returned. | [optional]
**components** | Option<**Vec<serde_json::Value>**> |  | [optional]
**rejected_reason** | Option<**String**> | Only when status is REJECTED. | [optional]
**quality_score** | Option<**serde_json::Value**> | Post-approval quality (GREEN/YELLOW/RED), when Meta reports one. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


