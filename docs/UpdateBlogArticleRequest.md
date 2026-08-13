# UpdateBlogArticleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | Option<**String**> |  | [optional]
**body_html** | Option<**String**> | Article body as HTML. | [optional]
**handle** | Option<**String**> | URL slug of the article. | [optional]
**tags** | Option<**Vec<String>**> | Replaces the full tag list. | [optional]
**author** | Option<**String**> | Display name of the article author. | [optional]
**excerpt** | Option<**String**> | Short summary shown in blog listings. | [optional]
**image** | Option<[**models::CreateBlogArticleRequestImage**](CreateBlogArticleRequestImage.md)> |  | [optional]
**seo** | Option<[**models::CreateBlogArticleRequestSeo**](CreateBlogArticleRequestSeo.md)> |  | [optional]
**is_published** | Option<**bool**> | Set false to unpublish the article back to a draft. | [optional]
**publish_date** | Option<**String**> | ISO 8601 datetime with offset (or Z). A future date schedules publication natively on the platform. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


