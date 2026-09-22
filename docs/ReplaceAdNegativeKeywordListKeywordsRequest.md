# ReplaceAdNegativeKeywordListKeywordsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id. | 
**ad_account_id** | Option<**String**> | Platform ad account ID (Google customer ID, digits only). Required when the connection has multiple customers. | [optional]
**customer_id** | Option<**String**> | Alias of adAccountId, kept for existing callers | [optional]
**platform** | Option<**Platform**> | Optional courtesy field. The resolved account or campaign determines support; other platforms return 501. (enum: facebook, instagram, tiktok, linkedin, pinterest, google, twitter, openai) | [optional]
**keywords** | [**Vec<models::KeywordEntry>**](KeywordEntry.md) | Full desired keyword set. Bare strings use broad match. Send [] to clear the list. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


