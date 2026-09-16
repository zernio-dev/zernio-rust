# \ProductsApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_product**](ProductsApi.md#get_product) | **GET** /v1/accounts/{accountId}/products/{productId} | Get a product
[**list_products**](ProductsApi.md#list_products) | **GET** /v1/accounts/{accountId}/products | List products
[**update_product**](ProductsApi.md#update_product) | **PATCH** /v1/accounts/{accountId}/products/{productId} | Update a product



## get_product

> models::GetProduct200Response get_product(account_id, product_id)
Get a product

Fetches a single product with its variants, options and images. `productId` is the platform's numeric product id from `GET /v1/accounts/{accountId}/products`, not a Zernio id.  Supported on Shopify (platform `shopify`); accounts on other platforms return 400. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify SocialAccount id. | [required] |
**product_id** | **String** | Platform-native numeric product id. Non-numeric values return 400. | [required] |

### Return type

[**models::GetProduct200Response**](getProduct_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_products

> models::ListProducts200Response list_products(account_id, limit, cursor, status, query)
List products

Lists the products on the connected store in the platform's default order, each with its variants, options and images. Cursor-paginated: pass `limit` (1-50, default 20) and the `cursor` from a previous response's `nextCursor`; `nextCursor` is null when there are no more pages. Filter with `status` and/or `query` (the platform's product search syntax, e.g. `title:*shirt* vendor:Acme tag:summer`).  Supported on Shopify (platform `shopify`); accounts on other platforms return 400. A store connected before product access was added answers 403 insufficient_permissions until the merchant reconnects it through `GET /v1/connect/shopify`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify SocialAccount id. | [required] |
**limit** | Option<**i32**> | Page size (1-50). |  |[default to 20]
**cursor** | Option<**String**> | Opaque cursor from a previous response. Omit for the first page. |  |
**status** | Option<**String**> | Only products in this status. |  |
**query** | Option<**String**> | Platform product search syntax, passed through verbatim (Shopify: title, vendor, product_type, tag, sku, handle, created_at, updated_at, ...). |  |

### Return type

[**models::ListProducts200Response**](listProducts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_product

> models::GetProduct200Response update_product(account_id, product_id, update_product_request)
Update a product

Partial-updates a product. Send any subset of `title`, `descriptionHtml`, `handle`, `vendor`, `productType`, `tags`, `status`, `seo` and `variants`; at least one field is required (an empty body returns 400). `tags` replaces the full tag list. `variants` updates the price and compare-at price of the listed variant ids only; other variants are untouched, and a variant id that does not belong to the product is a 400. Responds with the product as it is after the update.  Supported on Shopify (platform `shopify`); accounts on other platforms return 400. A store connected before product access was added answers 403 insufficient_permissions until the merchant reconnects it through `GET /v1/connect/shopify`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected Shopify SocialAccount id. | [required] |
**product_id** | **String** | Platform-native numeric product id. Non-numeric values return 400. | [required] |
**update_product_request** | [**UpdateProductRequest**](UpdateProductRequest.md) |  | [required] |

### Return type

[**models::GetProduct200Response**](getProduct_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

