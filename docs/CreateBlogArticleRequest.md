# CreateBlogArticleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **String** |  | 
**body_html** | Option<**String**> | Article body as HTML. | [optional]
**handle** | Option<**String**> | URL slug. Generated from the title when omitted. | [optional]
**tags** | Option<**Vec<String>**> | Tag names. WordPress resolves existing names case-insensitively and creates missing tags. | [optional]
**author** | Option<**String**> | Shopify author display name, or numeric WordPress user id serialized as a string. Assigning another WordPress user may require elevated capability. | [optional]
**excerpt** | Option<**String**> | Short summary shown in blog listings. | [optional]
**image** | Option<[**models::CreateBlogArticleRequestImage**](CreateBlogArticleRequestImage.md)> |  | [optional]
**seo** | Option<[**models::CreateBlogArticleRequestSeo**](CreateBlogArticleRequestSeo.md)> |  | [optional]
**is_published** | Option<**bool**> | Set false for a draft or true to publish. On WordPress false takes priority over a future publishDate; omission with no date defaults to draft. | [optional]
**publish_date** | Option<**String**> | ISO 8601 datetime with offset (or Z). A future date schedules publication natively on the platform. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


