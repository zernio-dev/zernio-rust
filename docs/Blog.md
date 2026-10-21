# Blog

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Platform-native blog id. Shopify uses a numeric blog id. WordPress.com uses the numeric site id; self-hosted WordPress and Wix use `1`, scoped to the connected account. Webflow uses the CMS collection id. | [optional]
**platform** | Option<**Platform**> |  (enum: shopify, wordpress, wix, webflow) | [optional]
**title** | Option<**String**> |  | [optional]
**handle** | Option<**String**> | URL slug on Shopify and Webflow (the collection slug); site hostname on WordPress and Wix. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


