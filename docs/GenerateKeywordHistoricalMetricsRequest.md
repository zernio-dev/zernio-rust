# GenerateKeywordHistoricalMetricsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio googleads SocialAccount id. | 
**ad_account_id** | Option<**String**> | Platform ad account ID (Google customer ID, digits only). | [optional]
**customer_id** | Option<**String**> | Alias of adAccountId, kept for existing callers | [optional]
**keywords** | **Vec<String>** |  | 
**countries** | Option<**Vec<String>**> | ISO 3166-1 alpha-2 country codes. Omitted = worldwide. | [optional]
**language_constant_id** | Option<**String**> | Google languageConstant id (1000 = English). | [optional][default to 1000]
**network** | Option<**Network**> |  (enum: GOOGLE_SEARCH, GOOGLE_SEARCH_AND_PARTNERS) | [optional][default to GoogleSearch]
**include_adult_keywords** | Option<**bool**> |  | [optional]
**include_average_cpc** | Option<**bool**> | Adds averageCpcMicros to each row's keywordMetrics. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


