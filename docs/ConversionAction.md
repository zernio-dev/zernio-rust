# ConversionAction

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **String** | Google Ads conversion action id. | 
**name** | **String** |  | 
**r#type** | **String** | Google's ConversionActionType, e.g. WEBPAGE, UPLOAD_CLICKS. | 
**status** | **String** | Google's ConversionActionStatus, e.g. ENABLED, REMOVED, HIDDEN. | 
**category** | **String** | Google's ConversionActionCategory, e.g. DEFAULT, PURCHASE, LEAD. | 
**tag_snippets** | [**Vec<models::ConversionActionTagSnippetsInner>**](ConversionActionTagSnippetsInner.md) | The code a customer pastes onto their site. Present for types Google generates a snippet for (e.g. WEBPAGE); empty otherwise.  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


