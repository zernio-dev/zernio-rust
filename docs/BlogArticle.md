# BlogArticle

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Platform-native article/post id: numeric on Shopify and WordPress, a GUID on Wix, a hex item id on Webflow. | [optional]
**blog_id** | Option<**String**> | Platform-native id of the blog the article belongs to. | [optional]
**platform** | Option<**Platform**> |  (enum: shopify, wordpress, wix, webflow) | [optional]
**title** | Option<**String**> |  | [optional]
**body_html** | Option<**String**> | Article body as HTML. Wix stores rich content, converted from and to HTML; Wix lists return null (get the article for its body). | [optional]
**handle** | Option<**String**> | URL slug of the article. | [optional]
**url** | Option<**String**> | WordPress and Wix. Public URL of the article while it is published; null for drafts and scheduled posts, and on a Wix site that is not published yet. | [optional]
**tags** | Option<**Vec<String>**> | Tag names. On WordPress and Wix, missing tag names are created and matching is case-insensitive. | [optional]
**author** | Option<**String**> | Shopify author display name, numeric WordPress user id serialized as a string, or Wix site member id. Wix posts without one are attributed to the site's default author. | [optional]
**excerpt** | Option<**String**> | Short summary shown in blog listings. | [optional]
**image** | Option<[**models::BlogArticleImage**](BlogArticleImage.md)> |  | [optional]
**is_published** | Option<**bool**> | False while the article is a draft or its publish date is still in the future. | [optional]
**published_at** | Option<**String**> | Publication time. On WordPress this is present only when status is `publish`; null for drafts, pending/private posts, and scheduled posts. | [optional]
**status** | Option<**Status**> | WordPress and Wix. Post status (`future` = scheduled, `pending` = in review on Wix); omitted for Shopify. (enum: publish, future, draft, pending, private) | [optional]
**publish_date** | Option<**String**> | WordPress and Wix. Scheduled publication time in UTC when status is `future`; null for other statuses and omitted for Shopify. | [optional]
**created_at** | Option<**String**> | Creation time when the platform exposes one. WordPress returns null because its core date is the editable publication date. | [optional]
**updated_at** | Option<**String**> | Last modification time. WordPress returns modified_gmt as UTC. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


