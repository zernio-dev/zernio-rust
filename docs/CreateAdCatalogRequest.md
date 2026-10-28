# CreateAdCatalogRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | A facebook, instagram, metaads or whatsapp account ID | 
**catalog_account_id** | Option<**String**> | Account whose Meta login token performs the call (see GET) | [optional]
**ad_account_id** | Option<**String**> | Ad account whose owner business creates the catalog | [optional]
**business_id** | Option<**String**> | Business portfolio that owns the catalog | [optional]
**name** | **String** |  | 
**vertical** | Option<**Vertical**> | Meta catalog vertical. Use services for a professional services catalog (for example one linked to WhatsApp). local_service_business is a deprecated alias of local_service_businesses. The product endpoints under /v1/ads/catalogs/{catalogId}/products write commerce product items only. (enum: commerce, adoptable_pets, apps_and_software, articles_and_publications, destinations, flights, generic, home_listings, hotels, local_service_businesses, media_titles, offer_items, offline_commerce, services, transactable_items, vehicles, local_service_business) | [optional][default to Commerce]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


