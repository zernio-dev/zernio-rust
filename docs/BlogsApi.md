# \BlogsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_blog**](BlogsApi.md#create_blog) | **POST** /v1/accounts/{accountId}/blogs | Create a blog
[**create_blog_article**](BlogsApi.md#create_blog_article) | **POST** /v1/accounts/{accountId}/blogs/{blogId}/articles | Create a blog article
[**delete_blog**](BlogsApi.md#delete_blog) | **DELETE** /v1/accounts/{accountId}/blogs/{blogId} | Delete a blog
[**delete_blog_article**](BlogsApi.md#delete_blog_article) | **DELETE** /v1/accounts/{accountId}/blogs/{blogId}/articles/{articleId} | Delete a blog article
[**get_blog**](BlogsApi.md#get_blog) | **GET** /v1/accounts/{accountId}/blogs/{blogId} | Get a blog
[**get_blog_article**](BlogsApi.md#get_blog_article) | **GET** /v1/accounts/{accountId}/blogs/{blogId}/articles/{articleId} | Get a blog article
[**list_blog_articles**](BlogsApi.md#list_blog_articles) | **GET** /v1/accounts/{accountId}/blogs/{blogId}/articles | List blog articles
[**list_blogs**](BlogsApi.md#list_blogs) | **GET** /v1/accounts/{accountId}/blogs | List blogs
[**update_blog**](BlogsApi.md#update_blog) | **PATCH** /v1/accounts/{accountId}/blogs/{blogId} | Update a blog
[**update_blog_article**](BlogsApi.md#update_blog_article) | **PATCH** /v1/accounts/{accountId}/blogs/{blogId}/articles/{articleId} | Update a blog article



## create_blog

> models::CreateBlog201Response create_blog(account_id, create_blog_request)
Create a blog

Creates a blog on the connected store. The platform generates the URL `handle` from the title when omitted.  Supported on Shopify (platform `shopify`). A WordPress or Wix connection is its existing site, so both return 405 for blog creation. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify SocialAccount id. | [required] |
**create_blog_request** | [**CreateBlogRequest**](CreateBlogRequest.md) |  | [required] |

### Return type

[**models::CreateBlog201Response**](createBlog_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_blog_article

> models::CreateBlogArticle201Response create_blog_article(account_id, blog_id, create_blog_article_request)
Create a blog article

Creates an article on the blog. Publishing behavior:  - WordPress, Wix and Webflow default to a draft when both publishing   fields are omitted. - `isPublished: false` keeps the article as a draft and takes priority   over a future `publishDate`. - A future `publishDate` schedules publication natively on the   platform; the platform publishes it at that time with no Zernio   queue involved. - `isPublished: true` publishes immediately when there is no future   `publishDate`. - `seo.title` / `seo.description` map to Shopify's global `title_tag`   and `description_tag` metafields (the fields Shopify themes read for   the page title and meta description), and on Wix to the post's SEO   title and meta description. WordPress and Webflow reject `seo`; SEO   plugin and custom-field writes are not supported. - Webflow has no scheduling API: a future `publishDate` returns 400   unless `isPublished: false` keeps a draft. Fields map to the   collection's own fields by type and slug (the body to its rich text   field, `excerpt` to a summary field, `image` to an image field, `tags`   and `author` to tag and author reference fields); sending a field the   collection does not have returns 400, as does a collection that   requires a field the Blogs API cannot fill. - Wix stores rich content: `bodyHtml` is converted on write (each   top-level HTML element must fit 30,000 characters), and images in   the body are imported into the site's Media Manager.  Supported on Shopify (`shopify`), WordPress (`wordpress`), Wix (`wix`) and Webflow (`webflow`). WordPress native scheduling depends on the site's scheduler/WP-Cron. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify, WordPress, Wix or Webflow account id. | [required] |
**blog_id** | **String** | Platform-native blog/site id returned by the list operation. | [required] |
**create_blog_article_request** | [**CreateBlogArticleRequest**](CreateBlogArticleRequest.md) |  | [required] |

### Return type

[**models::CreateBlogArticle201Response**](createBlogArticle_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_blog

> delete_blog(account_id, blog_id)
Delete a blog

Deletes the blog AND every article in it. The delete happens on the platform and is permanent; Zernio stores nothing to restore it from.  Supported on Shopify (platform `shopify`). Disconnect a WordPress or Wix account instead of deleting its site; both return 405 here. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify SocialAccount id. | [required] |
**blog_id** | **String** | Platform-native blog id. Shopify blog ids are numeric; other values return 400. | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_blog_article

> delete_blog_article(account_id, blog_id, article_id)
Delete a blog article

Deletes the article. The delete happens on the platform and is permanent; Zernio stores nothing to restore it from. On WordPress the post is force-deleted, while uploaded attachments and tags remain in the site's media library and taxonomy. On Webflow the item is unpublished from the live site, then deleted from the collection.  Supported on Shopify (`shopify`), WordPress (`wordpress`), Wix (`wix`) and Webflow (`webflow`). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify, WordPress, Wix or Webflow account id. | [required] |
**blog_id** | **String** | Platform-native blog/site id returned by the list operation. | [required] |
**article_id** | **String** | Platform-native article id: numeric on Shopify and WordPress, a GUID on Wix, a 24-character hex item id on Webflow. Other formats return 400. | [required] |

### Return type

 (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_blog

> models::GetBlog200Response get_blog(account_id, blog_id)
Get a blog

Fetches a single blog. Use the platform-native `blogId` returned by `GET /v1/accounts/{accountId}/blogs`: a Shopify numeric blog id, the WordPress.com numeric site id, or `1` for a self-hosted WordPress or a Wix site. That `1` is scoped to its connected account. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify, WordPress, Wix or Webflow account id. | [required] |
**blog_id** | **String** | Platform-native blog/site id returned by the list operation. | [required] |

### Return type

[**models::GetBlog200Response**](getBlog_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_blog_article

> models::CreateBlogArticle201Response get_blog_article(account_id, blog_id, article_id)
Get a blog article

Fetches a single article. An article addressed through a blog it does not belong to is a 404 (code blog_article_not_found).  Supported on Shopify (`shopify`), WordPress (`wordpress`), Wix (`wix`) and Webflow (`webflow`). WordPress returns its native `status`; `publishedAt` is present only for a published post and `publishDate` only for a scheduled post. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify, WordPress, Wix or Webflow account id. | [required] |
**blog_id** | **String** | Platform-native blog/site id returned by the list operation. | [required] |
**article_id** | **String** | Platform-native article id: numeric on Shopify and WordPress, a GUID on Wix, a 24-character hex item id on Webflow. Other formats return 400. | [required] |

### Return type

[**models::CreateBlogArticle201Response**](createBlogArticle_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_blog_articles

> models::ListBlogArticles200Response list_blog_articles(account_id, blog_id, limit, cursor)
List blog articles

Lists the articles of a blog. Cursor-paginated: pass `limit` (1-50, default 20) and the `cursor` from a previous response's `nextCursor`; `nextCursor` is null when there are no more pages. Treat cursors as opaque and pass them unchanged. Supported on Shopify (`shopify`), WordPress (`wordpress`), Wix (`wix`) and Webflow (`webflow`). WordPress and Wix results include `status` and include `publishDate` only for scheduled (`future`) posts. Wix lists return `bodyHtml: null`; get the article for its body. Webflow results report `status` as `publish` or `draft` only. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify, WordPress, Wix or Webflow account id. | [required] |
**blog_id** | **String** | Platform-native blog/site id returned by the list operation. | [required] |
**limit** | Option<**i32**> | Page size (1-50). |  |[default to 20]
**cursor** | Option<**String**> | Opaque cursor from a previous response. Omit for the first page. |  |

### Return type

[**models::ListBlogArticles200Response**](listBlogArticles_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_blogs

> models::ListBlogs200Response list_blogs(account_id, limit, cursor)
List blogs

Lists blogs on the connected account. Shopify returns its store blogs with cursor pagination. A WordPress or Wix account represents one site and always returns exactly that one blog with `nextCursor: null`. A Webflow site returns each CMS collection that has a rich text field (its blog id is the collection id), with `nextCursor: null`.  `limit` is 1-50 (default 20). Treat `nextCursor` as opaque; pass it unchanged on the next request. Supported on Shopify (`shopify`), WordPress (`wordpress`), Wix (`wix`) and Webflow (`webflow`). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify, WordPress, Wix or Webflow account id. | [required] |
**limit** | Option<**i32**> | Page size (1-50). |  |[default to 20]
**cursor** | Option<**String**> | Opaque cursor from a previous response. Omit for the first page. |  |

### Return type

[**models::ListBlogs200Response**](listBlogs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_blog

> models::CreateBlog201Response update_blog(account_id, blog_id, update_blog_request)
Update a blog

Partial-updates a blog. Send any subset of `title` and `handle`; at least one field is required (an empty body returns 400).  Supported on Shopify (platform `shopify`). WordPress and Wix site settings are not writable through this API, so both return 405. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify SocialAccount id. | [required] |
**blog_id** | **String** | Platform-native blog id. Shopify blog ids are numeric; other values return 400. | [required] |
**update_blog_request** | [**UpdateBlogRequest**](UpdateBlogRequest.md) |  | [required] |

### Return type

[**models::CreateBlog201Response**](createBlog_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_blog_article

> models::CreateBlogArticle201Response update_blog_article(account_id, blog_id, article_id, update_blog_article_request)
Update a blog article

Partial-updates an article. Send any subset of the create fields (`title`, `bodyHtml`, `handle`, `tags`, `author`, `excerpt`, `image`, `seo`, `isPublished`, `publishDate`); at least one field is required (an empty body returns 400). `isPublished` and `publishDate` behave as on create: `isPublished: false` unpublishes back to a draft and a future `publishDate` schedules publication natively on the platform. Omitting both fields preserves the current WordPress or Wix status. Omitting `image` preserves the current featured image; removal is not supported. WordPress rejects `seo` and does not support SEO-plugin/custom-field, category, or custom-post-type writes. On Webflow, an edit to a published item goes live immediately, `isPublished: false` unpublishes it, and a future `publishDate` returns 400.  Supported on Shopify (`shopify`), WordPress (`wordpress`), Wix (`wix`) and Webflow (`webflow`). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify, WordPress, Wix or Webflow account id. | [required] |
**blog_id** | **String** | Platform-native blog/site id returned by the list operation. | [required] |
**article_id** | **String** | Platform-native article id: numeric on Shopify and WordPress, a GUID on Wix, a 24-character hex item id on Webflow. Other formats return 400. | [required] |
**update_blog_article_request** | [**UpdateBlogArticleRequest**](UpdateBlogArticleRequest.md) |  | [required] |

### Return type

[**models::CreateBlogArticle201Response**](createBlogArticle_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

