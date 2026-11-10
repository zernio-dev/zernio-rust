# UpdateCreatorCampaignRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | Option<**String**> |  | [optional]
**brand_name** | Option<**String**> |  | [optional]
**platforms** | Option<**Vec<Platforms>**> |  (enum: tiktok, instagram, youtube, threads, pinterest, facebook, twitter) | [optional]
**content_rules** | Option<**String**> |  | [optional]
**starts_at** | Option<**String**> |  | [optional]
**ends_at** | Option<**String**> |  | [optional]
**tracking_days** | Option<**i32**> |  | [optional]
**hold_days** | Option<**i32**> |  | [optional]
**max_post_age_minutes** | Option<**i32**> | Null removes the limit. | [optional]
**settlement** | Option<**Settlement**> |  (enum: none, external, treasury) | [optional]
**economics** | Option<[**models::CreatorCampaignEconomics**](CreatorCampaignEconomics.md)> |  | [optional]
**caps** | Option<[**models::CreatorCampaignCaps**](CreatorCampaignCaps.md)> |  | [optional]
**branding** | Option<[**models::CreatorCampaignBranding**](CreatorCampaignBranding.md)> |  | [optional]
**landing_url** | Option<**String**> | The page creator tracking links open. Required unless `attribution` is `code`. | [optional]
**code_discount_percent** | Option<**i32**> | What each creator's discount code takes off an order. Required unless `attribution` is `link`. | [optional]
**auto_payout** | Option<[**models::CreatorCampaignAutoPayout**](CreatorCampaignAutoPayout.md)> |  | [optional]
**join_approval** | Option<**JoinApproval**> | manual holds creators who join through the open link as `pending` until you approve them. Personal invites are never held. (enum: auto, manual) | [optional]
**require_draft_approval** | Option<**bool**> | Creators upload a draft for review before publishing, and each submitted post must name an approved draft. | [optional]
**store_account_id** | Option<**String**> | A connected Shopify or WooCommerce store account. On `commission` and smart `retainer` economics its orders pay commission: required there, and fixed once such a campaign leaves draft.  On any campaign creators can ask for free samples of its products (`sampleProductIds`). Changing it without `sampleProductIds` clears the sample products; null removes the store and the products.  | [optional]
**sample_product_ids** | Option<**Vec<String>**> | Product ids in the store that creators can ask a free sample of. Each is read from the store and saved as `sampleProducts`; an unknown product answers 404 `product_not_found`. Needs a store, otherwise 400 `missing_required_field` (`param: storeAccountId`). | [optional]
**sample_content_due_days** | Option<**i32**> | Days after a sample is approved before a creator with no post since shows as owing content. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


