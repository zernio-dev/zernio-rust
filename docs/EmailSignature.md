# EmailSignature

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> |  | [optional]
**name** | Option<**String**> |  | [optional]
**html** | Option<**String**> |  | [optional]
**text** | Option<**String**> | Appended to plain-text bodies. When `null`, the html stripped to text is used. | [optional]
**account_id** | Option<**String**> | `null` for a workspace-wide signature. | [optional]
**default_for** | Option<**Vec<String>**> | Sending addresses this signature is the default for. Each address has one default per scope; an account signature wins over a workspace one. | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


