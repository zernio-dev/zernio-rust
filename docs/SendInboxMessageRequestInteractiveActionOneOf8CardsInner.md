# SendInboxMessageRequestInteractiveActionOneOf8CardsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**card_index** | Option<**i32**> | Card position. Auto-filled sequentially when omitted. | [optional]
**r#type** | Option<**String**> | `product` for a product card; media cards use `cta_url` or a quick-reply type. | [optional]
**header** | Option<**serde_json::Value**> | Media cards only | [optional]
**body** | Option<**serde_json::Value**> | Optional card body text. | [optional]
**action** | Option<**serde_json::Value**> | Product cards: `{ catalog_id, product_retailer_id }` (required). Media cards: the card's button action (e.g. `cta_url` with `parameters.display_text` and `parameters.url`). | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


