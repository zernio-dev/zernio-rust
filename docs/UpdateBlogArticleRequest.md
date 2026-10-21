# UpdateBlogArticleRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | Option<**String**> |  | [optional]
**body_html** | Option<**String**> | Article body as HTML. | [optional]
**handle** | Option<**String**> | URL slug of the article. | [optional]
**tags** | Option<**Vec<String>**> | Replaces the full tag-name list. WordPress and Wix resolve existing names case-insensitively and create missing tags (Wix allows up to 30). | [optional]
**author** | Option<**String**> | Shopify author display name, numeric WordPress user id serialized as a string, or Wix site member id. Assigning another WordPress user may require elevated capability. Wix posts without one go to the site's default author. | [optional]
**excerpt** | Option<**String**> | Short summary shown in blog listings. | [optional]
**image** | Option<[**models::UpdateBlogArticleRequestImage**](UpdateBlogArticleRequestImage.md)> |  | [optional]
**seo** | Option<[**models::CreateBlogArticleRequestSeo**](CreateBlogArticleRequestSeo.md)> |  | [optional]
**is_published** | Option<**bool**> | Set false to move to draft or true to publish. On WordPress and Wix false takes priority over a future publishDate; omission preserves status unless publishDate is sent (edits to a published Wix post go live). | [optional]
**publish_date** | Option<**String**> | ISO 8601 datetime with offset (or Z). A future date schedules publication natively on the platform. | [optional]
**field_data** | Option<**std::collections::HashMap<String, serde_json::Value>**> | Webflow only. The collection's own fields that the Blogs API does not map, keyed by field slug, in Webflow's value format (a Reference is an item id, an Image is { url, alt }). Required by collections with required fields of their own; a create that leaves one empty answers 400 listing them. A slug the API already fills (name, slug, body, summary, image, tags, author, date) or one the collection lacks answers 400. Other platforms answer 400. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


