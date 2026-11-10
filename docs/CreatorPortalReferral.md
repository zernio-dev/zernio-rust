# CreatorPortalReferral

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | Option<**String**> | The creator's discount code. Null while the store has not created it yet, or on a link-only campaign. | 
**discount_percent** | Option<**i32**> | What the code takes off an order. | 
**tracking_url** | Option<**String**> | The landing page with the UTM parameters that credit the creator. Null on a code-only campaign. | 
**orders** | [**Vec<models::CreatorPortalReferralOrdersInner>**](CreatorPortalReferralOrdersInner.md) | The latest 50 credited orders. | 
**totals** | [**models::CreatorPortalReferralTotals**](CreatorPortalReferralTotals.md) |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


