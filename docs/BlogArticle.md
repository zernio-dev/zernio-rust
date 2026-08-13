# BlogArticle

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Platform-native article id (numeric string for Shopify). | [optional]
**blog_id** | Option<**String**> | Platform-native id of the blog the article belongs to. | [optional]
**platform** | Option<**Platform**> |  (enum: shopify) | [optional]
**title** | Option<**String**> |  | [optional]
**body_html** | Option<**String**> | Article body as HTML. | [optional]
**handle** | Option<**String**> | URL slug of the article. | [optional]
**tags** | Option<**Vec<String>**> |  | [optional]
**author** | Option<**String**> | Display name of the article author. | [optional]
**excerpt** | Option<**String**> | Short summary shown in blog listings. | [optional]
**image** | Option<[**models::BlogArticleImage**](BlogArticleImage.md)> |  | [optional]
**is_published** | Option<**bool**> | False while the article is a draft or its publish date is still in the future. | [optional]
**published_at** | Option<**String**> | When the article was (or is scheduled to be) published; null for drafts. | [optional]
**created_at** | Option<**String**> |  | [optional]
**updated_at** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


