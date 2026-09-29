# CommerceStore

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** | Zernio SocialAccount id of the store. | 
**platform** | **Platform** |  (enum: shopify, woocommerce) | 
**name** | **String** |  | 
**domain** | **String** | The platform domain of the store, e.g. my-store.myshopify.com. | 
**url** | Option<**String**> | Public storefront URL. | 
**currency** | **String** | ISO 4217 code the store sells in. | 
**country** | Option<**String**> | ISO 3166-1 alpha-2 country of the store. | 
**capabilities** | [**Vec<models::CommerceCapability>**](CommerceCapability.md) |  | 
**missing_capabilities** | [**Vec<models::CommerceCapability>**](CommerceCapability.md) | Capabilities the platform supports that this store has not granted yet. | 
**grant_permissions_url** | Option<**String**> | Shopify: a page in the Shopify admin where the store owner approves the permissions missingCapabilities need, on the existing install (no reinstall; they can revoke them later). Null when nothing is missing or the store cannot grant them this way (a store connected with its own custom-app token). | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


