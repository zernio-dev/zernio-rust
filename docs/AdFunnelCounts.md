# AdFunnelCounts

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**landing_page_views** | Option<**i32**> | Landing page views: the visitor actually loaded the destination, unlike a link click. Meta `landing_page_view`. | [optional]
**content_views** | Option<**i32**> | Content views (Meta `ViewContent` pixel event). | [optional]
**searches** | Option<**i32**> | On-site searches (Meta `Search` pixel event). | [optional]
**wishlist_adds** | Option<**i32**> | Adds to wishlist (Meta `AddToWishlist` pixel event). | [optional]
**cart_adds** | Option<**i32**> | Adds to cart (Meta `AddToCart` pixel event). | [optional]
**checkouts_initiated** | Option<**i32**> | Checkouts started (Meta `InitiateCheckout` pixel event). | [optional]
**payment_info_adds** | Option<**i32**> | Payment details added at checkout (Meta `AddPaymentInfo` pixel event). | [optional]
**purchases** | Option<**i32**> | Purchases. Pair with `purchaseValue` for revenue.  **Meta** reports one purchase under several action types, so this takes the FIRST present, in this order, never a sum: `offsite_conversion.fb_pixel_purchase`, `omni_purchase`, `app_custom_event.fb_mobile_purchase`, `onsite_conversion.purchase`, `purchase`.  It always counts purchases, whatever the ad set optimizes for. `conversions` instead follows the ad set's optimization event (PURCHASE when none is named), so the two can differ on any other goal.  **TikTok:** app purchases (`purchase`), else website complete payments (`complete_payment`), else Place an Order (`place_order`).  | [optional]
**leads** | Option<**i32**> | Leads, from either the website pixel or an instant form, whichever the ad uses. | [optional]
**registrations_completed** | Option<**i32**> | Completed registrations (Meta `CompleteRegistration` pixel event). | [optional]
**app_installs** | Option<**i32**> | Mobile app installs attributed to the ad. | [optional]
**messaging_conversations_started** | Option<**i32**> | Messaging conversations started within 7 days, the headline metric for click-to-WhatsApp and click-to-Messenger ads. | [optional]
**messaging_first_replies** | Option<**i32**> | Messaging threads where the person sent a first reply. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


