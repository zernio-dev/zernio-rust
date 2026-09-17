# MetaCatalogProductInput

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**retailer_id** | Option<**String**> | Your SKU; unique inside the catalog | [optional]
**name** | Option<**String**> |  | [optional]
**description** | Option<**String**> |  | [optional]
**url** | Option<**String**> | Product page | [optional]
**image_url** | Option<**String**> |  | [optional]
**additional_image_urls** | Option<**Vec<String>**> |  | [optional]
**price** | Option<**f64**> | Major units, e.g. 12.99 | [optional]
**currency** | Option<**String**> | ISO 4217, e.g. EUR | [optional]
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


