# \CommerceApi

All URIs are relative to *https://zernio.com/api*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_commerce_discount_codes**](CommerceApi.md#add_commerce_discount_codes) | **POST** /v1/commerce/discounts/{discountId}/codes | Add codes to a discount
[**add_commerce_marketing_engagement**](CommerceApi.md#add_commerce_marketing_engagement) | **POST** /v1/commerce/marketing-activities/{remoteId}/engagements | Report daily engagement
[**add_commerce_product_images**](CommerceApi.md#add_commerce_product_images) | **POST** /v1/commerce/products/{productId}/images | Add images
[**change_collection_channels**](CommerceApi.md#change_collection_channels) | **POST** /v1/commerce/collections/{collectionId}/channels | Publish or unpublish a collection
[**change_commerce_collection_products**](CommerceApi.md#change_commerce_collection_products) | **POST** /v1/commerce/collections/{collectionId}/products | Add or remove products in a collection
[**change_commerce_inventory**](CommerceApi.md#change_commerce_inventory) | **POST** /v1/commerce/products/{productId}/inventory | Set or adjust stock
[**change_commerce_product_state**](CommerceApi.md#change_commerce_product_state) | **POST** /v1/commerce/products/state | Activate, deactivate, archive or delete products
[**change_commerce_product_tags**](CommerceApi.md#change_commerce_product_tags) | **POST** /v1/commerce/products/tags | Add or remove tags in bulk
[**change_product_channels**](CommerceApi.md#change_product_channels) | **POST** /v1/commerce/products/{productId}/channels | Publish or unpublish a product
[**create_commerce_catalog_sync**](CommerceApi.md#create_commerce_catalog_sync) | **POST** /v1/commerce/catalog-syncs | Sync a store into a Meta catalog
[**create_commerce_collection**](CommerceApi.md#create_commerce_collection) | **POST** /v1/commerce/collections | Create a collection
[**create_commerce_discount**](CommerceApi.md#create_commerce_discount) | **POST** /v1/commerce/discounts | Create a discount
[**create_commerce_menu**](CommerceApi.md#create_commerce_menu) | **POST** /v1/commerce/menus | Create a navigation menu
[**create_commerce_metaobject**](CommerceApi.md#create_commerce_metaobject) | **POST** /v1/commerce/metaobjects | Create a metaobject
[**create_commerce_page**](CommerceApi.md#create_commerce_page) | **POST** /v1/commerce/pages | Create a page
[**create_commerce_product**](CommerceApi.md#create_commerce_product) | **POST** /v1/commerce/products | Create a product
[**create_commerce_product_options**](CommerceApi.md#create_commerce_product_options) | **POST** /v1/commerce/products/{productId}/options | Add options
[**create_commerce_product_variants**](CommerceApi.md#create_commerce_product_variants) | **POST** /v1/commerce/products/{productId}/variants | Add variants
[**create_commerce_redirect**](CommerceApi.md#create_commerce_redirect) | **POST** /v1/commerce/redirects | Create a URL redirect
[**delete_collection_metafields**](CommerceApi.md#delete_collection_metafields) | **DELETE** /v1/commerce/collections/{collectionId}/metafields | Delete collection metafields
[**delete_commerce_catalog_sync**](CommerceApi.md#delete_commerce_catalog_sync) | **DELETE** /v1/commerce/catalog-syncs/{syncId} | Stop a catalog sync
[**delete_commerce_collection**](CommerceApi.md#delete_commerce_collection) | **DELETE** /v1/commerce/collections/{collectionId} | Delete a collection
[**delete_commerce_discount**](CommerceApi.md#delete_commerce_discount) | **DELETE** /v1/commerce/discounts/{discountId} | Delete a discount
[**delete_commerce_marketing_activity**](CommerceApi.md#delete_commerce_marketing_activity) | **DELETE** /v1/commerce/marketing-activities/{remoteId} | Delete a marketing activity
[**delete_commerce_menu**](CommerceApi.md#delete_commerce_menu) | **DELETE** /v1/commerce/menus/{menuId} | Delete a navigation menu
[**delete_commerce_metaobject**](CommerceApi.md#delete_commerce_metaobject) | **DELETE** /v1/commerce/metaobjects/{metaobjectId} | Delete a metaobject
[**delete_commerce_page**](CommerceApi.md#delete_commerce_page) | **DELETE** /v1/commerce/pages/{pageId} | Delete a page
[**delete_commerce_price_list_prices**](CommerceApi.md#delete_commerce_price_list_prices) | **DELETE** /v1/commerce/price-lists/{priceListId}/prices | Remove fixed prices
[**delete_commerce_product_options**](CommerceApi.md#delete_commerce_product_options) | **DELETE** /v1/commerce/products/{productId}/options | Delete options
[**delete_commerce_product_variants**](CommerceApi.md#delete_commerce_product_variants) | **DELETE** /v1/commerce/products/{productId}/variants | Delete variants
[**delete_commerce_redirect**](CommerceApi.md#delete_commerce_redirect) | **DELETE** /v1/commerce/redirects/{redirectId} | Delete a URL redirect
[**delete_product_metafields**](CommerceApi.md#delete_product_metafields) | **DELETE** /v1/commerce/products/{productId}/metafields | Delete product metafields
[**duplicate_commerce_product**](CommerceApi.md#duplicate_commerce_product) | **POST** /v1/commerce/products/{productId}/duplicate | Duplicate a product
[**get_commerce_catalog_sync**](CommerceApi.md#get_commerce_catalog_sync) | **GET** /v1/commerce/catalog-syncs/{syncId} | Get a catalog sync
[**get_commerce_collection**](CommerceApi.md#get_commerce_collection) | **GET** /v1/commerce/collections/{collectionId} | Get a collection
[**get_commerce_discount**](CommerceApi.md#get_commerce_discount) | **GET** /v1/commerce/discounts/{discountId} | Get a discount
[**get_commerce_menu**](CommerceApi.md#get_commerce_menu) | **GET** /v1/commerce/menus/{menuId} | Get a navigation menu
[**get_commerce_metaobject**](CommerceApi.md#get_commerce_metaobject) | **GET** /v1/commerce/metaobjects/{metaobjectId} | Get a metaobject
[**get_commerce_page**](CommerceApi.md#get_commerce_page) | **GET** /v1/commerce/pages/{pageId} | Get a page
[**get_commerce_product**](CommerceApi.md#get_commerce_product) | **GET** /v1/commerce/products/{productId} | Get a product
[**get_commerce_store**](CommerceApi.md#get_commerce_store) | **GET** /v1/commerce/store | Get a store
[**list_collection_metafields**](CommerceApi.md#list_collection_metafields) | **GET** /v1/commerce/collections/{collectionId}/metafields | List collection metafields
[**list_commerce_catalog_syncs**](CommerceApi.md#list_commerce_catalog_syncs) | **GET** /v1/commerce/catalog-syncs | List catalog syncs
[**list_commerce_channels**](CommerceApi.md#list_commerce_channels) | **GET** /v1/commerce/channels | List sales channels
[**list_commerce_collections**](CommerceApi.md#list_commerce_collections) | **GET** /v1/commerce/collections | List collections
[**list_commerce_discounts**](CommerceApi.md#list_commerce_discounts) | **GET** /v1/commerce/discounts | List discounts
[**list_commerce_inventory**](CommerceApi.md#list_commerce_inventory) | **GET** /v1/commerce/inventory | Get a product's stock
[**list_commerce_locations**](CommerceApi.md#list_commerce_locations) | **GET** /v1/commerce/locations | List locations
[**list_commerce_markets**](CommerceApi.md#list_commerce_markets) | **GET** /v1/commerce/markets | List markets
[**list_commerce_menus**](CommerceApi.md#list_commerce_menus) | **GET** /v1/commerce/menus | List navigation menus
[**list_commerce_metaobject_definitions**](CommerceApi.md#list_commerce_metaobject_definitions) | **GET** /v1/commerce/metaobject-definitions | List metaobject definitions
[**list_commerce_metaobjects**](CommerceApi.md#list_commerce_metaobjects) | **GET** /v1/commerce/metaobjects | List metaobjects of a type
[**list_commerce_pages**](CommerceApi.md#list_commerce_pages) | **GET** /v1/commerce/pages | List pages
[**list_commerce_price_lists**](CommerceApi.md#list_commerce_price_lists) | **GET** /v1/commerce/price-lists | List price lists
[**list_commerce_products**](CommerceApi.md#list_commerce_products) | **GET** /v1/commerce/products | List products
[**list_commerce_redirects**](CommerceApi.md#list_commerce_redirects) | **GET** /v1/commerce/redirects | List URL redirects
[**list_product_metafields**](CommerceApi.md#list_product_metafields) | **GET** /v1/commerce/products/{productId}/metafields | List product metafields
[**remove_commerce_product_images**](CommerceApi.md#remove_commerce_product_images) | **DELETE** /v1/commerce/products/{productId}/images | Remove images
[**reorder_commerce_collection_products**](CommerceApi.md#reorder_commerce_collection_products) | **POST** /v1/commerce/collections/{collectionId}/reorder | Reorder products in a collection
[**reorder_commerce_product_images**](CommerceApi.md#reorder_commerce_product_images) | **POST** /v1/commerce/products/{productId}/images/reorder | Reorder images
[**run_commerce_catalog_sync**](CommerceApi.md#run_commerce_catalog_sync) | **POST** /v1/commerce/catalog-syncs/{syncId}/run | Run a catalog sync now
[**set_collection_metafields**](CommerceApi.md#set_collection_metafields) | **PUT** /v1/commerce/collections/{collectionId}/metafields | Set collection metafields
[**set_commerce_discount_active**](CommerceApi.md#set_commerce_discount_active) | **POST** /v1/commerce/discounts/{discountId}/state | Activate or deactivate a discount
[**set_commerce_price_list_prices**](CommerceApi.md#set_commerce_price_list_prices) | **PUT** /v1/commerce/price-lists/{priceListId}/prices | Set fixed prices
[**set_product_metafields**](CommerceApi.md#set_product_metafields) | **PUT** /v1/commerce/products/{productId}/metafields | Set product metafields
[**update_commerce_collection**](CommerceApi.md#update_commerce_collection) | **PATCH** /v1/commerce/collections/{collectionId} | Update a collection
[**update_commerce_discount**](CommerceApi.md#update_commerce_discount) | **PATCH** /v1/commerce/discounts/{discountId} | Update a discount
[**update_commerce_menu**](CommerceApi.md#update_commerce_menu) | **PUT** /v1/commerce/menus/{menuId} | Replace a navigation menu
[**update_commerce_metaobject**](CommerceApi.md#update_commerce_metaobject) | **PATCH** /v1/commerce/metaobjects/{metaobjectId} | Update a metaobject
[**update_commerce_page**](CommerceApi.md#update_commerce_page) | **PATCH** /v1/commerce/pages/{pageId} | Update a page
[**update_commerce_product**](CommerceApi.md#update_commerce_product) | **PATCH** /v1/commerce/products/{productId} | Update a product
[**update_commerce_product_prices**](CommerceApi.md#update_commerce_product_prices) | **POST** /v1/commerce/products/{productId}/price | Update variant prices
[**update_commerce_redirect**](CommerceApi.md#update_commerce_redirect) | **PATCH** /v1/commerce/redirects/{redirectId} | Update a URL redirect
[**upsert_commerce_marketing_activity**](CommerceApi.md#upsert_commerce_marketing_activity) | **PUT** /v1/commerce/marketing-activities | Record a marketing activity



## add_commerce_discount_codes

> models::ReorderCommerceProductImages200Response add_commerce_discount_codes(discount_id, add_commerce_discount_codes_request)
Add codes to a discount

Adds up to 250 more codes to a code discount, for example one per influencer. The platform adds them in the background. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**discount_id** | **String** | Platform-native id. | [required] |
**add_commerce_discount_codes_request** | [**AddCommerceDiscountCodesRequest**](AddCommerceDiscountCodesRequest.md) |  | [required] |

### Return type

[**models::ReorderCommerceProductImages200Response**](reorderCommerceProductImages_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## add_commerce_marketing_engagement

> models::AddCommerceMarketingEngagement201Response add_commerce_marketing_engagement(remote_id, add_commerce_marketing_engagement_request)
Report daily engagement

Reports one day's numbers for an activity (UTC day), shown next to it in the store's Marketing section. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**remote_id** | **String** | The remoteId given when recording it. | [required] |
**add_commerce_marketing_engagement_request** | [**AddCommerceMarketingEngagementRequest**](AddCommerceMarketingEngagementRequest.md) |  | [required] |

### Return type

[**models::AddCommerceMarketingEngagement201Response**](addCommerceMarketingEngagement_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## add_commerce_product_images

> models::CreateCommerceProduct201Response add_commerce_product_images(product_id, add_commerce_product_images_request)
Add images

Adds images from public URLs. The platform fetches them, so they can appear on the product a few seconds after the call returns. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** | Platform-native id. | [required] |
**add_commerce_product_images_request** | [**AddCommerceProductImagesRequest**](AddCommerceProductImagesRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceProduct201Response**](createCommerceProduct_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## change_collection_channels

> models::ChangeCollectionChannels200Response change_collection_channels(collection_id, change_product_channels_request)
Publish or unpublish a collection

Publishes to and/or unpublishes from sales channels (the online store, Shop, POS and others). List channels with GET /v1/commerce/channels. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**collection_id** | **String** | Platform-native id. | [required] |
**change_product_channels_request** | [**ChangeProductChannelsRequest**](ChangeProductChannelsRequest.md) |  | [required] |

### Return type

[**models::ChangeCollectionChannels200Response**](changeCollectionChannels_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## change_commerce_collection_products

> models::ChangeCommerceCollectionProducts200Response change_commerce_collection_products(collection_id, change_commerce_collection_products_request)
Add or remove products in a collection

Adds and/or removes hand-picked products. Products a collection includes through its own rules are not affected. `pending` is true when the platform finishes the change in the background; the product count then catches up a few seconds later. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**collection_id** | **String** | Platform-native collection id. | [required] |
**change_commerce_collection_products_request** | [**ChangeCommerceCollectionProductsRequest**](ChangeCommerceCollectionProductsRequest.md) |  | [required] |

### Return type

[**models::ChangeCommerceCollectionProducts200Response**](changeCommerceCollectionProducts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## change_commerce_inventory

> models::ListCommerceInventory200Response change_commerce_inventory(product_id, change_commerce_inventory_request)
Set or adjust stock

`set` makes `quantity` the new available count; `adjust` adds `quantity` (negative to subtract). The variant must be stocked at the location. Answers the product's stock after the change. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** | Platform-native id. | [required] |
**change_commerce_inventory_request** | [**ChangeCommerceInventoryRequest**](ChangeCommerceInventoryRequest.md) |  | [required] |

### Return type

[**models::ListCommerceInventory200Response**](listCommerceInventory_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## change_commerce_product_state

> models::ChangeCommerceProductState200Response change_commerce_product_state(change_commerce_product_state_request)
Activate, deactivate, archive or delete products

Applies one action to up to 50 products and reports each product's outcome, so one failure does not abort the rest. On Shopify, `deactivate` sets the product to draft and `delete` is permanent. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**change_commerce_product_state_request** | [**ChangeCommerceProductStateRequest**](ChangeCommerceProductStateRequest.md) |  | [required] |

### Return type

[**models::ChangeCommerceProductState200Response**](changeCommerceProductState_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## change_commerce_product_tags

> models::ChangeCommerceProductTags200Response change_commerce_product_tags(change_commerce_product_tags_request)
Add or remove tags in bulk

Adds and/or removes tags on up to 50 products and reports each product's outcome. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**change_commerce_product_tags_request** | [**ChangeCommerceProductTagsRequest**](ChangeCommerceProductTagsRequest.md) |  | [required] |

### Return type

[**models::ChangeCommerceProductTags200Response**](changeCommerceProductTags_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## change_product_channels

> models::ChangeProductChannels200Response change_product_channels(product_id, change_product_channels_request)
Publish or unpublish a product

Publishes to and/or unpublishes from sales channels (the online store, Shop, POS and others). List channels with GET /v1/commerce/channels. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** | Platform-native id. | [required] |
**change_product_channels_request** | [**ChangeProductChannelsRequest**](ChangeProductChannelsRequest.md) |  | [required] |

### Return type

[**models::ChangeProductChannels200Response**](changeProductChannels_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_commerce_catalog_sync

> models::CreateCommerceCatalogSync202Response create_commerce_catalog_sync(create_commerce_catalog_sync_request)
Sync a store into a Meta catalog

Keeps a Meta product catalog in sync with the store, for catalog ads (`goal: catalog_sales`) and Shops. The first full run starts right away in the background; `runStatus` and the item counts report its outcome. Every active product variant that is published to the online store and has an image becomes a catalog item, grouped by product (`item_group_id`). After that, product changes on the store update the catalog within minutes, and a daily full run removes items for products or variants the store no longer has. Items are namespaced to the store, so a catalog can take several stores and a run never touches items it did not create.  `catalogAccountId` is a connected facebook, instagram or metaads account whose Meta login can manage the catalog (the catalog_management permission); find catalogs with `GET /v1/ads/catalogs`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_commerce_catalog_sync_request** | [**CreateCommerceCatalogSyncRequest**](CreateCommerceCatalogSyncRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceCatalogSync202Response**](createCommerceCatalogSync_202_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_commerce_collection

> models::CreateCommerceCollection201Response create_commerce_collection(create_commerce_collection_request)
Create a collection

Creates a collection, optionally with hand-picked products. On Shopify the collection starts unpublished from the online store; publish it from the Shopify admin. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_commerce_collection_request** | [**CreateCommerceCollectionRequest**](CreateCommerceCollectionRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceCollection201Response**](createCommerceCollection_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_commerce_discount

> models::CreateCommerceDiscount201Response create_commerce_discount(create_commerce_discount_request)
Create a discount

Creates a code discount (buyers enter a code) or an automatic one (applied at checkout), as a percentage, a fixed amount or free shipping. It applies to every product unless productIds or collectionIds narrow it, and to every buyer. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_commerce_discount_request** | [**CreateCommerceDiscountRequest**](CreateCommerceDiscountRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceDiscount201Response**](createCommerceDiscount_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_commerce_menu

> models::CreateCommerceMenu201Response create_commerce_menu(create_commerce_menu_request)
Create a navigation menu

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_commerce_menu_request** | [**CreateCommerceMenuRequest**](CreateCommerceMenuRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceMenu201Response**](createCommerceMenu_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_commerce_metaobject

> models::CreateCommerceMetaobject201Response create_commerce_metaobject(create_commerce_metaobject_request)
Create a metaobject

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_commerce_metaobject_request** | [**CreateCommerceMetaobjectRequest**](CreateCommerceMetaobjectRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceMetaobject201Response**](createCommerceMetaobject_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_commerce_page

> models::CreateCommercePage201Response create_commerce_page(create_commerce_page_request)
Create a page

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_commerce_page_request** | [**CreateCommercePageRequest**](CreateCommercePageRequest.md) |  | [required] |

### Return type

[**models::CreateCommercePage201Response**](createCommercePage_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_commerce_product

> models::CreateCommerceProduct201Response create_commerce_product(create_commerce_product_request)
Create a product

Creates a product with its options and variants. `status` defaults to `draft`: no platform offers a sandbox for product writes, so nothing goes on sale unless you ask for `active`. A product without `options` has exactly one variant. Images are fetched by the platform from the given URLs and may appear on the product a few seconds later. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_commerce_product_request** | [**CreateCommerceProductRequest**](CreateCommerceProductRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceProduct201Response**](createCommerceProduct_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_commerce_product_options

> models::CreateCommerceProduct201Response create_commerce_product_options(product_id, create_commerce_product_options_request)
Add options

Adds option axes (e.g. Size, Color) and their values. With createVariants true the platform creates a variant for every new combination; otherwise existing variants take the first value. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** | Platform-native id. | [required] |
**create_commerce_product_options_request** | [**CreateCommerceProductOptionsRequest**](CreateCommerceProductOptionsRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceProduct201Response**](createCommerceProduct_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_commerce_product_variants

> models::CreateCommerceProduct201Response create_commerce_product_variants(product_id, create_commerce_product_variants_request)
Add variants

Adds variants to a product. Each variant names a value for every product option (create options first with POST .../options). A product's placeholder default variant is replaced when real ones arrive. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** | Platform-native id. | [required] |
**create_commerce_product_variants_request** | [**CreateCommerceProductVariantsRequest**](CreateCommerceProductVariantsRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceProduct201Response**](createCommerceProduct_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## create_commerce_redirect

> models::CreateCommerceRedirect201Response create_commerce_redirect(create_commerce_redirect_request)
Create a URL redirect

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**create_commerce_redirect_request** | [**CreateCommerceRedirectRequest**](CreateCommerceRedirectRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceRedirect201Response**](createCommerceRedirect_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_collection_metafields

> models::DeleteProductMetafields200Response delete_collection_metafields(collection_id, account_id, keys)
Delete collection metafields

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**collection_id** | **String** | Platform-native id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |
**keys** | **String** | Comma-separated namespace.key pairs. | [required] |

### Return type

[**models::DeleteProductMetafields200Response**](deleteProductMetafields_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_commerce_catalog_sync

> models::DeleteCommerceCatalogSync200Response delete_commerce_catalog_sync(sync_id)
Stop a catalog sync

Stops syncing. Items already in the catalog stay there.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sync_id** | **String** |  | [required] |

### Return type

[**models::DeleteCommerceCatalogSync200Response**](deleteCommerceCatalogSync_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_commerce_collection

> models::DeleteCommerceCollection200Response delete_commerce_collection(collection_id, account_id)
Delete a collection

Deletes the collection. Its products are not affected.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**collection_id** | **String** | Platform-native collection id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::DeleteCommerceCollection200Response**](deleteCommerceCollection_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_commerce_discount

> models::DeleteCommerceDiscount200Response delete_commerce_discount(discount_id, account_id)
Delete a discount

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**discount_id** | **String** | Platform-native id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::DeleteCommerceDiscount200Response**](deleteCommerceDiscount_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_commerce_marketing_activity

> models::DeleteCommerceMarketingActivity200Response delete_commerce_marketing_activity(remote_id, account_id)
Delete a marketing activity

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**remote_id** | **String** | The remoteId given when recording it. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::DeleteCommerceMarketingActivity200Response**](deleteCommerceMarketingActivity_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_commerce_menu

> models::DeleteCommerceMenu200Response delete_commerce_menu(menu_id, account_id)
Delete a navigation menu

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**menu_id** | **String** | Platform-native id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::DeleteCommerceMenu200Response**](deleteCommerceMenu_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_commerce_metaobject

> models::DeleteCommerceMetaobject200Response delete_commerce_metaobject(metaobject_id, account_id)
Delete a metaobject

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**metaobject_id** | **String** | Platform-native id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::DeleteCommerceMetaobject200Response**](deleteCommerceMetaobject_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_commerce_page

> models::DeleteCommercePage200Response delete_commerce_page(page_id, account_id)
Delete a page

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page_id** | **String** | Platform-native id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::DeleteCommercePage200Response**](deleteCommercePage_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_commerce_price_list_prices

> models::DeleteCommercePriceListPrices200Response delete_commerce_price_list_prices(price_list_id, account_id, variant_ids)
Remove fixed prices

The variants go back to the market's converted price. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**price_list_id** | **String** | Platform-native id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |
**variant_ids** | **String** | Comma-separated ids. | [required] |

### Return type

[**models::DeleteCommercePriceListPrices200Response**](deleteCommercePriceListPrices_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_commerce_product_options

> models::CreateCommerceProduct201Response delete_commerce_product_options(product_id, account_id, names)
Delete options

Deletes options by name, with the variants that depended on them. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** | Platform-native id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |
**names** | **String** | Comma-separated option names. | [required] |

### Return type

[**models::CreateCommerceProduct201Response**](createCommerceProduct_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_commerce_product_variants

> models::CreateCommerceProduct201Response delete_commerce_product_variants(product_id, account_id, variant_ids)
Delete variants

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** | Platform-native id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |
**variant_ids** | **String** | Comma-separated ids. | [required] |

### Return type

[**models::CreateCommerceProduct201Response**](createCommerceProduct_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_commerce_redirect

> models::DeleteCommerceRedirect200Response delete_commerce_redirect(redirect_id, account_id)
Delete a URL redirect

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**redirect_id** | **String** | Platform-native id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::DeleteCommerceRedirect200Response**](deleteCommerceRedirect_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## delete_product_metafields

> models::DeleteProductMetafields200Response delete_product_metafields(product_id, account_id, keys)
Delete product metafields

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** | Platform-native id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |
**keys** | **String** | Comma-separated namespace.key pairs. | [required] |

### Return type

[**models::DeleteProductMetafields200Response**](deleteProductMetafields_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## duplicate_commerce_product

> models::CreateCommerceProduct201Response duplicate_commerce_product(product_id, duplicate_commerce_product_request)
Duplicate a product

Copies a product with its options, variants and (by default) images. The copy starts as a draft. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** | Platform-native id. | [required] |
**duplicate_commerce_product_request** | [**DuplicateCommerceProductRequest**](DuplicateCommerceProductRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceProduct201Response**](createCommerceProduct_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_commerce_catalog_sync

> models::CreateCommerceCatalogSync202Response get_commerce_catalog_sync(sync_id)
Get a catalog sync

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sync_id** | **String** |  | [required] |

### Return type

[**models::CreateCommerceCatalogSync202Response**](createCommerceCatalogSync_202_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_commerce_collection

> models::CreateCommerceCollection201Response get_commerce_collection(collection_id, account_id)
Get a collection

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**collection_id** | **String** | Platform-native collection id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::CreateCommerceCollection201Response**](createCommerceCollection_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_commerce_discount

> models::CreateCommerceDiscount201Response get_commerce_discount(discount_id, account_id)
Get a discount

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**discount_id** | **String** | Platform-native id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::CreateCommerceDiscount201Response**](createCommerceDiscount_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_commerce_menu

> models::CreateCommerceMenu201Response get_commerce_menu(menu_id, account_id)
Get a navigation menu

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**menu_id** | **String** | Platform-native id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::CreateCommerceMenu201Response**](createCommerceMenu_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_commerce_metaobject

> models::CreateCommerceMetaobject201Response get_commerce_metaobject(metaobject_id, account_id)
Get a metaobject

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**metaobject_id** | **String** | Platform-native id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::CreateCommerceMetaobject201Response**](createCommerceMetaobject_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_commerce_page

> models::CreateCommercePage201Response get_commerce_page(page_id, account_id)
Get a page

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page_id** | **String** | Platform-native id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::CreateCommercePage201Response**](createCommercePage_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_commerce_product

> models::CreateCommerceProduct201Response get_commerce_product(product_id, account_id)
Get a product

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** | Platform-native product id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::CreateCommerceProduct201Response**](createCommerceProduct_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## get_commerce_store

> models::GetCommerceStore200Response get_commerce_store(account_id)
Get a store

Returns the connected store with its currency, country and the `capabilities` it supports, so an integration can tell up front which Commerce operations the store serves. On Shopify, stock, sales channels, discounts, navigation, metaobjects, markets, marketing and image removal need permissions the store owner approves separately: `missingCapabilities` lists what is not granted yet and `grantPermissionsUrl` is the page where the owner approves it. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::GetCommerceStore200Response**](getCommerceStore_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_collection_metafields

> models::ListProductMetafields200Response list_collection_metafields(collection_id, account_id)
List collection metafields

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**collection_id** | **String** | Platform-native id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::ListProductMetafields200Response**](listProductMetafields_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_commerce_catalog_syncs

> models::ListCommerceCatalogSyncs200Response list_commerce_catalog_syncs(account_id)
List catalog syncs

The ad-platform catalogs this store is kept in sync with.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::ListCommerceCatalogSyncs200Response**](listCommerceCatalogSyncs_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_commerce_channels

> models::ListCommerceChannels200Response list_commerce_channels(account_id)
List sales channels

Where products and collections can be published: the online store, Shop, POS and installed channel apps. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::ListCommerceChannels200Response**](listCommerceChannels_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_commerce_collections

> models::ListCommerceCollections200Response list_commerce_collections(account_id, limit, cursor, query)
List collections

Lists the store's product collections. Cursor-paginated like products. List a collection's products with `GET /v1/commerce/products?collectionId=...`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | [required] |
**limit** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> |  |  |
**query** | Option<**String**> | Platform collection search syntax (Shopify: title, handle, collection_type, ...). |  |

### Return type

[**models::ListCommerceCollections200Response**](listCommerceCollections_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_commerce_discounts

> models::ListCommerceDiscounts200Response list_commerce_discounts(account_id, limit, cursor, query)
List discounts

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | [required] |
**limit** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> |  |  |
**query** | Option<**String**> | Platform search syntax, passed through. |  |

### Return type

[**models::ListCommerceDiscounts200Response**](listCommerceDiscounts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_commerce_inventory

> models::ListCommerceInventory200Response list_commerce_inventory(account_id, product_id)
Get a product's stock

Stock per variant and location: available, on hand, committed to orders and incoming. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | [required] |
**product_id** | **String** |  | [required] |

### Return type

[**models::ListCommerceInventory200Response**](listCommerceInventory_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_commerce_locations

> models::ListCommerceLocations200Response list_commerce_locations(account_id)
List locations

The store's stock locations (warehouses, shops). 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::ListCommerceLocations200Response**](listCommerceLocations_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_commerce_markets

> models::ListCommerceMarkets200Response list_commerce_markets(account_id)
List markets

The regions the store sells to, each with its own currency and pricing. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::ListCommerceMarkets200Response**](listCommerceMarkets_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_commerce_menus

> models::ListCommerceMenus200Response list_commerce_menus(account_id)
List navigation menus

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::ListCommerceMenus200Response**](listCommerceMenus_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_commerce_metaobject_definitions

> models::ListCommerceMetaobjectDefinitions200Response list_commerce_metaobject_definitions(account_id)
List metaobject definitions

The custom content types defined on the store and their fields. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::ListCommerceMetaobjectDefinitions200Response**](listCommerceMetaobjectDefinitions_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_commerce_metaobjects

> models::ListCommerceMetaobjects200Response list_commerce_metaobjects(account_id, r#type, limit, cursor)
List metaobjects of a type

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | [required] |
**r#type** | **String** | Definition type from GET /v1/commerce/metaobject-definitions. | [required] |
**limit** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> |  |  |

### Return type

[**models::ListCommerceMetaobjects200Response**](listCommerceMetaobjects_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_commerce_pages

> models::ListCommercePages200Response list_commerce_pages(account_id, limit, cursor, query)
List pages

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | [required] |
**limit** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> |  |  |
**query** | Option<**String**> | Platform search syntax, passed through. |  |

### Return type

[**models::ListCommercePages200Response**](listCommercePages_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_commerce_price_lists

> models::ListCommercePriceLists200Response list_commerce_price_lists(account_id)
List price lists

Price lists hold fixed prices per variant for a market. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::ListCommercePriceLists200Response**](listCommercePriceLists_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_commerce_products

> models::ListCommerceProducts200Response list_commerce_products(account_id, limit, cursor, status, query, collection_id)
List products

Lists the store's products with their variants, options and images. Cursor-paginated: pass `limit` (1-100, default 20) and the `cursor` from a previous response's `nextCursor`, which is null on the last page. Filter with `status` and/or `query` (the platform's product search syntax, passed through verbatim). A status the platform has no equivalent of returns an empty page. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | [required] |
**limit** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> | Opaque cursor from a previous response. Omit for the first page. |  |
**status** | Option<[**CommerceProductStatus**](CommerceProductStatus.md)> |  |  |
**query** | Option<**String**> | Platform product search syntax (Shopify: title, vendor, product_type, tag, sku, handle, ...). |  |
**collection_id** | Option<**String**> | Only products in this collection. |  |

### Return type

[**models::ListCommerceProducts200Response**](listCommerceProducts_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_commerce_redirects

> models::ListCommerceRedirects200Response list_commerce_redirects(account_id, limit, cursor, query)
List URL redirects

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**account_id** | **String** | Connected store SocialAccount id. | [required] |
**limit** | Option<**i32**> |  |  |[default to 20]
**cursor** | Option<**String**> |  |  |
**query** | Option<**String**> | Platform search syntax, passed through. |  |

### Return type

[**models::ListCommerceRedirects200Response**](listCommerceRedirects_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## list_product_metafields

> models::ListProductMetafields200Response list_product_metafields(product_id, account_id)
List product metafields

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** | Platform-native id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |

### Return type

[**models::ListProductMetafields200Response**](listProductMetafields_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## remove_commerce_product_images

> models::CreateCommerceProduct201Response remove_commerce_product_images(product_id, account_id, image_ids)
Remove images

Removes images from the product by image id (the `id` on each image). The file stays in the store's media library. Needs the products.images_remove capability. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** | Platform-native id. | [required] |
**account_id** | **String** | Connected store SocialAccount id. | [required] |
**image_ids** | **String** | Comma-separated ids. | [required] |

### Return type

[**models::CreateCommerceProduct201Response**](createCommerceProduct_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reorder_commerce_collection_products

> models::ReorderCommerceProductImages200Response reorder_commerce_collection_products(collection_id, reorder_commerce_collection_products_request)
Reorder products in a collection

Moves products to new 0-based positions. Only for collections sorted `manual`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**collection_id** | **String** | Platform-native id. | [required] |
**reorder_commerce_collection_products_request** | [**ReorderCommerceCollectionProductsRequest**](ReorderCommerceCollectionProductsRequest.md) |  | [required] |

### Return type

[**models::ReorderCommerceProductImages200Response**](reorderCommerceProductImages_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## reorder_commerce_product_images

> models::ReorderCommerceProductImages200Response reorder_commerce_product_images(product_id, reorder_commerce_product_images_request)
Reorder images

Puts the product's images in the given order; the first becomes the featured image. `pending` is true while the platform finishes in the background. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** | Platform-native id. | [required] |
**reorder_commerce_product_images_request** | [**ReorderCommerceProductImagesRequest**](ReorderCommerceProductImagesRequest.md) |  | [required] |

### Return type

[**models::ReorderCommerceProductImages200Response**](reorderCommerceProductImages_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## run_commerce_catalog_sync

> models::CreateCommerceCatalogSync202Response run_commerce_catalog_sync(sync_id)
Run a catalog sync now

Queues a full run. Poll GET /v1/commerce/catalog-syncs/{syncId} for the outcome.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**sync_id** | **String** |  | [required] |

### Return type

[**models::CreateCommerceCatalogSync202Response**](createCommerceCatalogSync_202_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_collection_metafields

> models::ListProductMetafields200Response set_collection_metafields(collection_id, set_product_metafields_request)
Set collection metafields

Creates or updates custom fields by namespace and key. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**collection_id** | **String** | Platform-native id. | [required] |
**set_product_metafields_request** | [**SetProductMetafieldsRequest**](SetProductMetafieldsRequest.md) |  | [required] |

### Return type

[**models::ListProductMetafields200Response**](listProductMetafields_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_commerce_discount_active

> models::CreateCommerceDiscount201Response set_commerce_discount_active(discount_id, set_commerce_discount_active_request)
Activate or deactivate a discount

Deactivating ends the discount now; activating starts it now. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**discount_id** | **String** | Platform-native id. | [required] |
**set_commerce_discount_active_request** | [**SetCommerceDiscountActiveRequest**](SetCommerceDiscountActiveRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceDiscount201Response**](createCommerceDiscount_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_commerce_price_list_prices

> models::SetCommercePriceListPrices200Response set_commerce_price_list_prices(price_list_id, set_commerce_price_list_prices_request)
Set fixed prices

Sets fixed prices for variants in the price list's currency, overriding the converted price in that market. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**price_list_id** | **String** | Platform-native id. | [required] |
**set_commerce_price_list_prices_request** | [**SetCommercePriceListPricesRequest**](SetCommercePriceListPricesRequest.md) |  | [required] |

### Return type

[**models::SetCommercePriceListPrices200Response**](setCommercePriceListPrices_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## set_product_metafields

> models::ListProductMetafields200Response set_product_metafields(product_id, set_product_metafields_request)
Set product metafields

Creates or updates custom fields by namespace and key. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** | Platform-native id. | [required] |
**set_product_metafields_request** | [**SetProductMetafieldsRequest**](SetProductMetafieldsRequest.md) |  | [required] |

### Return type

[**models::ListProductMetafields200Response**](listProductMetafields_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_commerce_collection

> models::CreateCommerceCollection201Response update_commerce_collection(collection_id, update_commerce_collection_request)
Update a collection

Partial update; at least one field besides accountId is required. Change membership with POST /v1/commerce/collections/{collectionId}/products.

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**collection_id** | **String** | Platform-native collection id. | [required] |
**update_commerce_collection_request** | [**UpdateCommerceCollectionRequest**](UpdateCommerceCollectionRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceCollection201Response**](createCommerceCollection_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_commerce_discount

> models::CreateCommerceDiscount201Response update_commerce_discount(discount_id, update_commerce_discount_request)
Update a discount

Changes a percentage, fixed-amount or free-shipping discount. Buy-X-get-Y and app discounts are read-only here. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**discount_id** | **String** | Platform-native id. | [required] |
**update_commerce_discount_request** | [**UpdateCommerceDiscountRequest**](UpdateCommerceDiscountRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceDiscount201Response**](createCommerceDiscount_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_commerce_menu

> models::CreateCommerceMenu201Response update_commerce_menu(menu_id, update_commerce_menu_request)
Replace a navigation menu

Replaces the title and the whole item tree. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**menu_id** | **String** | Platform-native id. | [required] |
**update_commerce_menu_request** | [**UpdateCommerceMenuRequest**](UpdateCommerceMenuRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceMenu201Response**](createCommerceMenu_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_commerce_metaobject

> models::CreateCommerceMetaobject201Response update_commerce_metaobject(metaobject_id, update_commerce_metaobject_request)
Update a metaobject

Sets the given field values; fields left out keep theirs. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**metaobject_id** | **String** | Platform-native id. | [required] |
**update_commerce_metaobject_request** | [**UpdateCommerceMetaobjectRequest**](UpdateCommerceMetaobjectRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceMetaobject201Response**](createCommerceMetaobject_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_commerce_page

> models::CreateCommercePage201Response update_commerce_page(page_id, update_commerce_page_request)
Update a page

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**page_id** | **String** | Platform-native id. | [required] |
**update_commerce_page_request** | [**UpdateCommercePageRequest**](UpdateCommercePageRequest.md) |  | [required] |

### Return type

[**models::CreateCommercePage201Response**](createCommercePage_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_commerce_product

> models::CreateCommerceProduct201Response update_commerce_product(product_id, update_commerce_product_request)
Update a product

Partial-updates the product's own fields; at least one besides `accountId` is required. `tags` replaces the full list. Change prices with `POST /v1/commerce/products/{productId}/price` and status with `POST /v1/commerce/products/state`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** | Platform-native product id. | [required] |
**update_commerce_product_request** | [**UpdateCommerceProductRequest**](UpdateCommerceProductRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceProduct201Response**](createCommerceProduct_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_commerce_product_prices

> models::CreateCommerceProduct201Response update_commerce_product_prices(product_id, update_commerce_product_prices_request)
Update variant prices

Sets the price and/or compare-at price of the listed variants. Other variants are untouched. Amounts are in the store currency; send `compareAtPrice: null` to remove a strike-through price. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**product_id** | **String** | Platform-native product id. | [required] |
**update_commerce_product_prices_request** | [**UpdateCommerceProductPricesRequest**](UpdateCommerceProductPricesRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceProduct201Response**](createCommerceProduct_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## update_commerce_redirect

> models::CreateCommerceRedirect201Response update_commerce_redirect(redirect_id, update_commerce_redirect_request)
Update a URL redirect

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**redirect_id** | **String** | Platform-native id. | [required] |
**update_commerce_redirect_request** | [**UpdateCommerceRedirectRequest**](UpdateCommerceRedirectRequest.md) |  | [required] |

### Return type

[**models::CreateCommerceRedirect201Response**](createCommerceRedirect_201_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)


## upsert_commerce_marketing_activity

> models::UpsertCommerceMarketingActivity200Response upsert_commerce_marketing_activity(upsert_commerce_marketing_activity_request)
Record a marketing activity

Creates or updates (by `remoteId`) an activity in the store's Marketing section, so the merchant sees a post, ad or message you ran for them, with its link and UTM parameters for attribution. Use your own id (for example the Zernio post or ad id) as `remoteId`. 

### Parameters


Name | Type | Description  | Required | Notes
------------- | ------------- | ------------- | ------------- | -------------
**upsert_commerce_marketing_activity_request** | [**UpsertCommerceMarketingActivityRequest**](UpsertCommerceMarketingActivityRequest.md) |  | [required] |

### Return type

[**models::UpsertCommerceMarketingActivity200Response**](upsertCommerceMarketingActivity_200_response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: application/json
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

