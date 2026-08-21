# BillingSnapshot

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**billing_system** | Option<**BillingSystem**> |  (enum: metronome, stripe, shopify) | [optional]
**plan** | Option<[**models::BillingSnapshotPlan**](BillingSnapshotPlan.md)> |  | [optional]
**shopify_shop_domain** | Option<**String**> | myshopify.com domain owning the subscription; present only when billingSystem is shopify. | [optional]
**period** | Option<[**models::BillingSnapshotPeriod**](BillingSnapshotPeriod.md)> |  | [optional]
**balance** | Option<[**models::BillingSnapshotBalance**](BillingSnapshotBalance.md)> |  | [optional]
**caps** | Option<[**models::BillingSnapshotCaps**](BillingSnapshotCaps.md)> |  | [optional]
**status** | Option<[**models::BillingSnapshotStatus**](BillingSnapshotStatus.md)> |  | [optional]
**legacy** | Option<[**models::BillingSnapshotLegacy**](BillingSnapshotLegacy.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


