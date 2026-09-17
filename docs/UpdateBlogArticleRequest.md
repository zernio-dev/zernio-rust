# UpdateBlogArticleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | Option<**String**> |  | [optional]
**body_html** | Option<**String**> | Article body as HTML. | [optional]
**handle** | Option<**String**> | URL slug of the article. | [optional]
**tags** | Option<**Vec<String>**> | Replaces the full tag-name list. WordPress resolves existing names case-insensitively and creates missing tags. | [optional]
**author** | Option<**String**> | Shopify author display name, or numeric WordPress user id serialized as a string. Assigning another WordPress user may require elevated capability. | [optional]
**excerpt** | Option<**String**> | Short summary shown in blog listings. | [optional]
**image** | Option<[**models::UpdateBlogArticleRequestImage**](UpdateBlogArticleRequestImage.md)> |  | [optional]
**seo** | Option<[**models::CreateBlogArticleRequestSeo**](CreateBlogArticleRequestSeo.md)> |  | [optional]
**is_published** | Option<**bool**> | Set false to move to draft or true to publish. On WordPress false takes priority over a future publishDate; omission preserves status unless publishDate is sent. | [optional]
**publish_date** | Option<**String**> | ISO 8601 datetime with offset (or Z). A future date schedules publication natively on the platform. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


