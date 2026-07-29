# GenerateKeywordIdeasRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio googleads SocialAccount id. | 
**customer_id** | Option<**String**> | Numeric Google Ads customer id (no dashes); only needed when the connection has several accounts. | [optional]
**seed_keywords** | Option<**Vec<String>**> | Seed terms. Provide these, seedUrl, or both. | [optional]
**seed_url** | Option<**String**> | Landing page to mine for ideas. Provide this, seedKeywords, or both. | [optional]
**countries** | Option<**Vec<String>**> | ISO 3166-1 alpha-2 country codes. Omitted = worldwide. | [optional]
**language_constant_id** | Option<**String**> | Google languageConstant id (1000 = English). | [optional][default to 1000]
**network** | Option<**Network**> |  (enum: GOOGLE_SEARCH, GOOGLE_SEARCH_AND_PARTNERS) | [optional][default to GoogleSearch]
**include_adult_keywords** | Option<**bool**> |  | [optional]
**page_size** | Option<**i32**> |  | [optional]
**page_token** | Option<**String**> | Cursor from paging.nextPageToken of the previous page. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


