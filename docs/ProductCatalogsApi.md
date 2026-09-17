# \ProductCatalogsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**batch_ad_catalog_products**](ProductCatalogsApi.md#batch_ad_catalog_products) | **POST** /v1/ads/catalogs/{catalogId}/products/batch | Create, update or delete products in bulk
[**create_ad_catalog**](ProductCatalogsApi.md#create_ad_catalog) | **POST** /v1/ads/catalogs | Create a Meta product catalog
[**create_ad_catalog_feed**](ProductCatalogsApi.md#create_ad_catalog_feed) | **POST** /v1/ads/catalogs/{catalogId}/feeds | Create a product feed
[**create_ad_catalog_feed_upload**](ProductCatalogsApi.md#create_ad_catalog_feed_upload) | **POST** /v1/ads/catalogs/{catalogId}/feeds/{feedId}/uploads | Fetch a feed file now
[**create_ad_catalog_product**](ProductCatalogsApi.md#create_ad_catalog_product) | **POST** /v1/ads/catalogs/{catalogId}/products | Add a product to a catalog
[**create_ad_catalog_product_set**](ProductCatalogsApi.md#create_ad_catalog_product_set) | **POST** /v1/ads/catalogs/{catalogId}/product-sets | Create a product set
[**delete_ad_catalog**](ProductCatalogsApi.md#delete_ad_catalog) | **DELETE** /v1/ads/catalogs/{catalogId} | Delete a product catalog
[**delete_ad_catalog_product**](ProductCatalogsApi.md#delete_ad_catalog_product) | **DELETE** /v1/ads/catalogs/{catalogId}/products/{productId} | Delete a product
[**delete_ad_catalog_product_set**](ProductCatalogsApi.md#delete_ad_catalog_product_set) | **DELETE** /v1/ads/catalogs/{catalogId}/product-sets/{productSetId} | Delete a product set
[**get_ad_catalog**](ProductCatalogsApi.md#get_ad_catalog) | **GET** /v1/ads/catalogs/{catalogId} | Get a product catalog
[**get_ad_catalog_batch**](ProductCatalogsApi.md#get_ad_catalog_batch) | **GET** /v1/ads/catalogs/{catalogId}/batches/{handle} | Get a bulk request's status
[**get_ad_catalog_product**](ProductCatalogsApi.md#get_ad_catalog_product) | **GET** /v1/ads/catalogs/{catalogId}/products/{productId} | Get a product
[**list_ad_catalog_feed_uploads**](ProductCatalogsApi.md#list_ad_catalog_feed_uploads) | **GET** /v1/ads/catalogs/{catalogId}/feeds/{feedId}/uploads | List a feed's uploads
[**list_ad_catalog_feeds**](ProductCatalogsApi.md#list_ad_catalog_feeds) | **GET** /v1/ads/catalogs/{catalogId}/feeds | List a catalog's product feeds
[**list_ad_catalog_product_sets**](ProductCatalogsApi.md#list_ad_catalog_product_sets) | **GET** /v1/ads/catalogs/{catalogId}/product-sets | List a catalog's product sets
[**list_ad_catalog_products**](ProductCatalogsApi.md#list_ad_catalog_products) | **GET** /v1/ads/catalogs/{catalogId}/products | List a catalog's products
[**list_ad_catalogs**](ProductCatalogsApi.md#list_ad_catalogs) | **GET** /v1/ads/catalogs | List Meta product catalogs
[**update_ad_catalog_product**](ProductCatalogsApi.md#update_ad_catalog_product) | **PUT** /v1/ads/catalogs/{catalogId}/products/{productId} | Update a product
[**update_ad_catalog_product_set**](ProductCatalogsApi.md#update_ad_catalog_product_set) | **PUT** /v1/ads/catalogs/{catalogId}/product-sets/{productSetId} | Update a product set



## batch_ad_catalog_products

> models::BatchAdCatalogProducts202Response batch_ad_catalog_products(catalog_id, batch_ad_catalog_products_request)
Create, update or delete products in bulk

Up to 5000 CREATE / UPDATE / DELETE requests keyed by `retailerId`, processed asynchronously by Meta. Returns handles; poll GET /v1/ads/catalogs/{catalogId}/batches/{handle} for the outcome and per-item errors. CREATE requests need name, url, imageUrl, price and currency.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**catalog_id** | **String** | Meta product catalog ID (from GET /v1/ads/catalogs) | [required] |
**batch_ad_catalog_products_request** | [**BatchAdCatalogProductsRequest**](BatchAdCatalogProductsRequest.md) |  | [required] |

### Return type

[**models::BatchAdCatalogProducts202Response**](batchAdCatalogProducts_202_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_ad_catalog

> models::CreateAdCatalog201Response create_ad_catalog(create_ad_catalog_request)
Create a Meta product catalog

Creates a Meta Commerce catalog in the business portfolio (resolved like GET). The same catalog serves Advantage+ catalog ads, Instagram/Facebook Shops and the WhatsApp Business catalog: link it to a WhatsApp number with POST /v1/whatsapp/catalogs. Needs catalog_management on the Meta login.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_ad_catalog_request** | [**CreateAdCatalogRequest**](CreateAdCatalogRequest.md) |  | [required] |

### Return type

[**models::CreateAdCatalog201Response**](createAdCatalog_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_ad_catalog_feed

> models::CreateAdCatalogFeed201Response create_ad_catalog_feed(catalog_id, create_ad_catalog_feed_request)
Create a product feed

A feed pulls a CSV/TSV/XML product file from a URL. With `schedule` Meta fetches it on a cadence; without it, trigger fetches with POST /v1/ads/catalogs/{catalogId}/feeds/{feedId}/uploads.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**catalog_id** | **String** | Meta product catalog ID (from GET /v1/ads/catalogs) | [required] |
**create_ad_catalog_feed_request** | [**CreateAdCatalogFeedRequest**](CreateAdCatalogFeedRequest.md) |  | [required] |

### Return type

[**models::CreateAdCatalogFeed201Response**](createAdCatalogFeed_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_ad_catalog_feed_upload

> models::CreateAdCatalogFeedUpload202Response create_ad_catalog_feed_upload(catalog_id, feed_id, create_ad_catalog_feed_upload_request)
Fetch a feed file now

Asks Meta to fetch the product file at `url` into the feed. Processing is asynchronous: read the outcome with GET uploads.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**catalog_id** | **String** | Meta product catalog ID (from GET /v1/ads/catalogs) | [required] |
**feed_id** | **String** |  | [required] |
**create_ad_catalog_feed_upload_request** | [**CreateAdCatalogFeedUploadRequest**](CreateAdCatalogFeedUploadRequest.md) |  | [required] |

### Return type

[**models::CreateAdCatalogFeedUpload202Response**](createAdCatalogFeedUpload_202_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_ad_catalog_product

> models::CreateAdCatalogProduct201Response create_ad_catalog_product(catalog_id, create_ad_catalog_product_request)
Add a product to a catalog

Adds one product. `retailerId` is your SKU and stays the handle for later lookups and batch updates. For many products at once use POST /v1/ads/catalogs/{catalogId}/products/batch. Needs catalog_management on the Meta login.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**catalog_id** | **String** | Meta product catalog ID (from GET /v1/ads/catalogs) | [required] |
**create_ad_catalog_product_request** | [**CreateAdCatalogProductRequest**](CreateAdCatalogProductRequest.md) |  | [required] |

### Return type

[**models::CreateAdCatalogProduct201Response**](createAdCatalogProduct_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_ad_catalog_product_set

> models::CreateAdCatalogProductSet201Response create_ad_catalog_product_set(catalog_id, create_ad_catalog_product_set_request)
Create a product set

A product set is a filter over the catalog, e.g. `{\"retailer_id\": {\"is_any\": [\"sku-1\", \"sku-2\"]}}` or `{\"brand\": {\"i_contains\": \"acme\"}}` (Meta's product set filter syntax).

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**catalog_id** | **String** | Meta product catalog ID (from GET /v1/ads/catalogs) | [required] |
**create_ad_catalog_product_set_request** | [**CreateAdCatalogProductSetRequest**](CreateAdCatalogProductSetRequest.md) |  | [required] |

### Return type

[**models::CreateAdCatalogProductSet201Response**](createAdCatalogProductSet_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_ad_catalog

> models::DeleteAdCatalog200Response delete_ad_catalog(catalog_id, account_id, catalog_account_id)
Delete a product catalog

Deletes the catalog and every product in it on Meta. Ads and WhatsApp numbers that use it lose their catalog.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**catalog_id** | **String** | Meta product catalog ID (from GET /v1/ads/catalogs) | [required] |
**account_id** | **String** | A facebook, instagram, metaads or whatsapp account ID | [required] |
**catalog_account_id** | Option<**String**> | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own |  |

### Return type

[**models::DeleteAdCatalog200Response**](deleteAdCatalog_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_ad_catalog_product

> models::DeleteAdCatalogProduct200Response delete_ad_catalog_product(catalog_id, product_id, account_id, catalog_account_id)
Delete a product

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**catalog_id** | **String** | Meta product catalog ID (from GET /v1/ads/catalogs) | [required] |
**product_id** | **String** | Meta product item ID (from the products list; not the retailer id) | [required] |
**account_id** | **String** | A facebook, instagram, metaads or whatsapp account ID | [required] |
**catalog_account_id** | Option<**String**> | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own |  |

### Return type

[**models::DeleteAdCatalogProduct200Response**](deleteAdCatalogProduct_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_ad_catalog_product_set

> models::DeleteAdCatalogProductSet200Response delete_ad_catalog_product_set(catalog_id, product_set_id, account_id, catalog_account_id)
Delete a product set

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**catalog_id** | **String** | Meta product catalog ID (from GET /v1/ads/catalogs) | [required] |
**product_set_id** | **String** |  | [required] |
**account_id** | **String** | A facebook, instagram, metaads or whatsapp account ID | [required] |
**catalog_account_id** | Option<**String**> | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own |  |

### Return type

[**models::DeleteAdCatalogProductSet200Response**](deleteAdCatalogProductSet_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_catalog

> models::CreateAdCatalog201Response get_ad_catalog(catalog_id, account_id, catalog_account_id)
Get a product catalog

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**catalog_id** | **String** | Meta product catalog ID (from GET /v1/ads/catalogs) | [required] |
**account_id** | **String** | A facebook, instagram, metaads or whatsapp account ID | [required] |
**catalog_account_id** | Option<**String**> | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own |  |

### Return type

[**models::CreateAdCatalog201Response**](createAdCatalog_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_catalog_batch

> models::GetAdCatalogBatch200Response get_ad_catalog_batch(catalog_id, handle, account_id, catalog_account_id)
Get a bulk request's status

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**catalog_id** | **String** | Meta product catalog ID (from GET /v1/ads/catalogs) | [required] |
**handle** | **String** | Handle returned by the batch call | [required] |
**account_id** | **String** | A facebook, instagram, metaads or whatsapp account ID | [required] |
**catalog_account_id** | Option<**String**> | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own |  |

### Return type

[**models::GetAdCatalogBatch200Response**](getAdCatalogBatch_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_ad_catalog_product

> models::CreateAdCatalogProduct201Response get_ad_catalog_product(catalog_id, product_id, account_id, catalog_account_id)
Get a product

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**catalog_id** | **String** | Meta product catalog ID (from GET /v1/ads/catalogs) | [required] |
**product_id** | **String** | Meta product item ID (from the products list; not the retailer id) | [required] |
**account_id** | **String** | A facebook, instagram, metaads or whatsapp account ID | [required] |
**catalog_account_id** | Option<**String**> | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own |  |

### Return type

[**models::CreateAdCatalogProduct201Response**](createAdCatalogProduct_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_catalog_feed_uploads

> models::ListAdCatalogFeedUploads200Response list_ad_catalog_feed_uploads(catalog_id, feed_id, account_id, catalog_account_id)
List a feed's uploads

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**catalog_id** | **String** | Meta product catalog ID (from GET /v1/ads/catalogs) | [required] |
**feed_id** | **String** |  | [required] |
**account_id** | **String** | A facebook, instagram, metaads or whatsapp account ID | [required] |
**catalog_account_id** | Option<**String**> | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own |  |

### Return type

[**models::ListAdCatalogFeedUploads200Response**](listAdCatalogFeedUploads_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_catalog_feeds

> models::ListAdCatalogFeeds200Response list_ad_catalog_feeds(catalog_id, account_id, catalog_account_id)
List a catalog's product feeds

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**catalog_id** | **String** | Meta product catalog ID (from GET /v1/ads/catalogs) | [required] |
**account_id** | **String** | A facebook, instagram, metaads or whatsapp account ID | [required] |
**catalog_account_id** | Option<**String**> | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own |  |

### Return type

[**models::ListAdCatalogFeeds200Response**](listAdCatalogFeeds_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_catalog_product_sets

> models::ListAdCatalogProductSets200Response list_ad_catalog_product_sets(catalog_id, account_id, catalog_account_id)
List a catalog's product sets

Lists a Meta product catalog's product sets, the unit a catalog ad promotes. Pass the chosen set id, not the parent catalog id, as `promotedObject.productSetId` on POST /v1/ads/create with `goal: catalog_sales`.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**catalog_id** | **String** | Meta product catalog ID (from GET /v1/ads/catalogs) | [required] |
**account_id** | **String** | A facebook, instagram, metaads or whatsapp account ID | [required] |
**catalog_account_id** | Option<**String**> | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own |  |

### Return type

[**models::ListAdCatalogProductSets200Response**](listAdCatalogProductSets_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_catalog_products

> models::ListAdCatalogProducts200Response list_ad_catalog_products(catalog_id, account_id, catalog_account_id, limit, after, retailer_id)
List a catalog's products

Pages through the catalog's products. Filter by your own `retailerId` to look one up. `price` and `salePrice` come back formatted by Meta (for example \"€49.90\").

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**catalog_id** | **String** | Meta product catalog ID (from GET /v1/ads/catalogs) | [required] |
**account_id** | **String** | A facebook, instagram, metaads or whatsapp account ID | [required] |
**catalog_account_id** | Option<**String**> | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token performs the call instead of the account's own |  |
**limit** | Option<**i32**> |  |  |[default to 25]
**after** | Option<**String**> | Cursor from the previous page's `nextCursor` |  |
**retailer_id** | Option<**String**> | Only the product with this retailer id (your SKU) |  |

### Return type

[**models::ListAdCatalogProducts200Response**](listAdCatalogProducts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_ad_catalogs

> models::ListAdCatalogs200Response list_ad_catalogs(account_id, catalog_account_id, ad_account_id, business_id)
List Meta product catalogs

Lists the Meta Commerce catalogs of a business portfolio (owned + agency-shared). The business comes from `businessId`, else the ad account's owner (`adAccountId`), else the WhatsApp Business Account's owner when `accountId` is a WhatsApp connection, else the only business the Meta login can see. Reads work with scopes customers already granted.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | A facebook, instagram, metaads or whatsapp account ID | [required] |
**catalog_account_id** | Option<**String**> | A facebook, instagram or metaads account whose Meta login carries catalog_management; its token is used instead of the account's own (needed for WhatsApp connections, whose token cannot manage catalogs). |  |
**ad_account_id** | Option<**String**> | Meta ad account ID (act_...) whose owner business to list |  |
**business_id** | Option<**String**> | Meta business portfolio ID to list |  |

### Return type

[**models::ListAdCatalogs200Response**](listAdCatalogs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad_catalog_product

> models::CreateAdCatalogProduct201Response update_ad_catalog_product(catalog_id, product_id, update_ad_catalog_product_request)
Update a product

Partial update: only the fields sent change. `retailerId` cannot change.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**catalog_id** | **String** | Meta product catalog ID (from GET /v1/ads/catalogs) | [required] |
**product_id** | **String** | Meta product item ID (from the products list; not the retailer id) | [required] |
**update_ad_catalog_product_request** | [**UpdateAdCatalogProductRequest**](UpdateAdCatalogProductRequest.md) |  | [required] |

### Return type

[**models::CreateAdCatalogProduct201Response**](createAdCatalogProduct_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_ad_catalog_product_set

> models::CreateAdCatalogProductSet201Response update_ad_catalog_product_set(catalog_id, product_set_id, update_ad_catalog_product_set_request)
Update a product set

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**catalog_id** | **String** | Meta product catalog ID (from GET /v1/ads/catalogs) | [required] |
**product_set_id** | **String** |  | [required] |
**update_ad_catalog_product_set_request** | [**UpdateAdCatalogProductSetRequest**](UpdateAdCatalogProductSetRequest.md) |  | [required] |

### Return type

[**models::CreateAdCatalogProductSet201Response**](createAdCatalogProductSet_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

