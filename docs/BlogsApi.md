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

Creates a blog on the connected store. The platform generates the URL `handle` from the title when omitted.  Supported on Shopify (platform `shopify`). A WordPress connection is its existing site, so WordPress returns 405 for blog creation. 

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

Creates an article on the blog. Publishing behavior:  - WordPress defaults to a draft when both publishing fields are omitted. - `isPublished: false` keeps the article as a draft and takes priority   over a future `publishDate`. - A future `publishDate` schedules publication natively on the   platform; the platform publishes it at that time with no Zernio   queue involved. - `isPublished: true` publishes immediately when there is no future   `publishDate`. - `seo.title` / `seo.description` map to Shopify's global `title_tag`   and `description_tag` metafields (the fields Shopify themes read for   the page title and meta description). WordPress rejects `seo`; SEO   plugin and custom-field writes are not supported.  Supported on Shopify (`shopify`) and WordPress (`wordpress`). WordPress native scheduling depends on the site's scheduler/WP-Cron. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify or WordPress account id. | [required] |
**blog_id** | **String** | Platform-native numeric blog/site id returned by the list operation. | [required] |
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

Deletes the blog AND every article in it. The delete happens on the platform and is permanent; Zernio stores nothing to restore it from.  Supported on Shopify (platform `shopify`). Disconnect a WordPress account instead of deleting its site; WordPress returns 405 here. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify SocialAccount id. | [required] |
**blog_id** | **String** | Platform-native numeric blog id. Non-numeric values return 400. | [required] |

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

Deletes the article. The delete happens on the platform and is permanent; Zernio stores nothing to restore it from. On WordPress the post is force-deleted, while uploaded attachments and tags remain in the site's media library and taxonomy.  Supported on Shopify (`shopify`) and WordPress (`wordpress`). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify or WordPress account id. | [required] |
**blog_id** | **String** | Platform-native numeric blog/site id returned by the list operation. | [required] |
**article_id** | **String** | Platform-native numeric article id. Non-numeric values return 400. | [required] |

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

Fetches a single blog. Use the platform-native `blogId` returned by `GET /v1/accounts/{accountId}/blogs`: a Shopify numeric blog id, the WordPress.com numeric site id, or `1` for a self-hosted WordPress site. The self-hosted id is scoped to its connected account. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify or WordPress account id. | [required] |
**blog_id** | **String** | Platform-native numeric blog/site id returned by the list operation. | [required] |

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

Fetches a single article. An article addressed through a blog it does not belong to is a 404 (code blog_article_not_found).  Supported on Shopify (`shopify`) and WordPress (`wordpress`). WordPress returns its native `status`; `publishedAt` is present only for a published post and `publishDate` only for a scheduled post. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify or WordPress account id. | [required] |
**blog_id** | **String** | Platform-native numeric blog/site id returned by the list operation. | [required] |
**article_id** | **String** | Platform-native numeric article id. Non-numeric values return 400. | [required] |

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

Lists the articles of a blog. Cursor-paginated: pass `limit` (1-50, default 20) and the `cursor` from a previous response's `nextCursor`; `nextCursor` is null when there are no more pages. Treat cursors as opaque and pass them unchanged. Supported on Shopify (`shopify`) and WordPress (`wordpress`). WordPress results include native `status` and include `publishDate` only for scheduled (`future`) posts. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify or WordPress account id. | [required] |
**blog_id** | **String** | Platform-native numeric blog/site id returned by the list operation. | [required] |
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

Lists blogs on the connected account. Shopify returns its store blogs with cursor pagination. A WordPress account represents one site and always returns exactly that one blog with `nextCursor: null`.  `limit` is 1-50 (default 20). Treat `nextCursor` as opaque; pass it unchanged on the next request. Supported on Shopify (`shopify`) and WordPress (`wordpress`). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify or WordPress account id. | [required] |
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

Partial-updates a blog. Send any subset of `title` and `handle`; at least one field is required (an empty body returns 400).  Supported on Shopify (platform `shopify`). WordPress site settings are not writable through this API, so WordPress returns 405. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify SocialAccount id. | [required] |
**blog_id** | **String** | Platform-native numeric blog id. Non-numeric values return 400. | [required] |
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

Partial-updates an article. Send any subset of the create fields (`title`, `bodyHtml`, `handle`, `tags`, `author`, `excerpt`, `image`, `seo`, `isPublished`, `publishDate`); at least one field is required (an empty body returns 400). `isPublished` and `publishDate` behave as on create: `isPublished: false` unpublishes back to a draft and a future `publishDate` schedules publication natively on the platform. Omitting both fields preserves the current WordPress status. Omitting `image` preserves the current featured image; removal is not supported. WordPress rejects `seo` and does not support SEO-plugin/custom-field, category, or custom-post-type writes.  Supported on Shopify (`shopify`) and WordPress (`wordpress`). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify or WordPress account id. | [required] |
**blog_id** | **String** | Platform-native numeric blog/site id returned by the list operation. | [required] |
**article_id** | **String** | Platform-native numeric article id. Non-numeric values return 400. | [required] |
**update_blog_article_request** | [**UpdateBlogArticleRequest**](UpdateBlogArticleRequest.md) |  | [required] |

### Return type

[**models::CreateBlogArticle201Response**](createBlogArticle_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

