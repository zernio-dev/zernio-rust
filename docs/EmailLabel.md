# EmailLabel

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Gmail label id such as `Label_12`, or the Outlook category name. | [optional]
**account_id** | Option<**String**> |  | [optional]
**provider** | Option<**Provider**> |  (enum: google, microsoft, imap) | [optional]
**name** | Option<**String**> | Gmail nests labels with a slash, as in `Hermia/Handled`. | [optional]
**r#type** | Option<**Type**> |  (enum: system, user) | [optional]
**color** | Option<[**models::EmailLabelColor**](EmailLabelColor.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


