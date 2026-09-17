# CreateAdCatalogProductRequestProduct

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**retailer_id** | **String** | Your SKU; unique inside the catalog | 
**name** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**url** | **String** | Product page | 
**image_url** | **String** |  | 
**additional_image_urls** | Option<**Vec<String>**> |  | [optional]
**price** | **f64** | Major units, e.g. 12.99 | 
**currency** | **String** | ISO 4217, e.g. EUR | 
**sale_price** | Option<**f64**> |  | [optional]
**sale_price_start_date** | Option<**String**> | ISO 8601 | [optional]
**sale_price_end_date** | Option<**String**> | ISO 8601 | [optional]
**availability** | Option<**Availability**> |  (enum: in stock, out of stock, preorder, available for order, discontinued, pending) | [optional]
**condition** | Option<**Condition**> |  (enum: new, refurbished, used) | [optional]
**brand** | Option<**String**> |  | [optional]
**category** | Option<**String**> |  | [optional]
**google_product_category** | Option<**String**> |  | [optional]
**product_type** | Option<**String**> |  | [optional]
**gtin** | Option<**String**> |  | [optional]
**mpn** | Option<**String**> |  | [optional]
**inventory** | Option<**i32**> |  | [optional]
**visibility** | Option<**Visibility**> |  (enum: published, staging) | [optional]
**color** | Option<**String**> |  | [optional]
**size** | Option<**String**> |  | [optional]
**gender** | Option<**Gender**> |  (enum: female, male, unisex) | [optional]
**material** | Option<**String**> |  | [optional]
**pattern** | Option<**String**> |  | [optional]
**custom_label0** | Option<**String**> |  | [optional]
**custom_label1** | Option<**String**> |  | [optional]
**custom_label2** | Option<**String**> |  | [optional]
**custom_label3** | Option<**String**> |  | [optional]
**custom_label4** | Option<**String**> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


