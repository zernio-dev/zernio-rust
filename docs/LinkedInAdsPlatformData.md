# LinkedInAdsPlatformData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cost_type** | Option<**CostType**> | Campaign cost model (billing event). Defaults to `CPM`. Required when `unitCost` is set so the manual bid applies to an explicit cost model.  (enum: CPM, CPC, CPV) | [optional]
**unit_cost** | Option<**f64**> | Manual bid in WHOLE account-currency units (e.g. 2.5 = $2.50). Requires `costType`. Omit for LinkedIn's automated (max delivery) bidding. LinkedIn enforces its own per-audience min/max bid bounds.  | [optional]
**optimization_target_type** | Option<**String**> | Campaign `optimizationTargetType` (e.g. `MAX_CLICK`, `TARGET_COST_PER_CLICK`, `MAX_IMPRESSION`). Forwarded verbatim, LinkedIn validates compatibility with the objective and `costType`. Omit for the objective-derived default: `awareness` gets `MAX_IMPRESSION`, `video_views` gets `MAX_VIDEO_VIEW`, and every other goal gets `MAX_CLICK`. `lead_generation` and `conversions` also get `MAX_CLICK`, because `MAX_LEAD` and `MAX_CONVERSION` need a lead gen form or a conversion rule that neither creation flow attaches. The default applies only to `SPONSORED_UPDATES` campaigns (every boost, and the image, video and carousel standalone ads), never to the `TEXT_AD`, `DYNAMIC` and `SPONSORED_INMAILS` campaigns the other creative formats produce. It is also skipped when `unitCost` or a non-`CPM` `costType` is set, since those select manual bidding and the bid is then yours to choose.  | [optional]
**creative_selection** | Option<**CreativeSelection**> | How LinkedIn rotates creatives within the campaign. Defaults to `OPTIMIZED`. (enum: OPTIMIZED, ROUND_ROBIN) | [optional]
**audience_expansion_enabled** | Option<**bool**> | Enable LinkedIn audience expansion. Defaults to false. | [optional]
**offsite_delivery_enabled** | Option<**bool**> | Deliver on the LinkedIn Audience Network. Defaults to false. | [optional]
**connected_television_only** | Option<**bool**> | Restrict delivery to Connected TV inventory. | [optional]
**carousel** | Option<[**models::LinkedInAdsPlatformDataCarousel**](LinkedInAdsPlatformDataCarousel.md)> |  | [optional]
**document** | Option<[**models::LinkedInAdsPlatformDataDocument**](LinkedInAdsPlatformDataDocument.md)> |  | [optional]
**spotlight** | Option<[**models::LinkedInAdsPlatformDataSpotlight**](LinkedInAdsPlatformDataSpotlight.md)> |  | [optional]
**follower** | Option<[**models::LinkedInAdsPlatformDataFollower**](LinkedInAdsPlatformDataFollower.md)> |  | [optional]
**jobs** | Option<[**models::LinkedInAdsPlatformDataJobs**](LinkedInAdsPlatformDataJobs.md)> |  | [optional]
**text_ad** | Option<[**models::LinkedInAdsPlatformDataTextAd**](LinkedInAdsPlatformDataTextAd.md)> |  | [optional]
**conversation** | Option<[**models::LinkedInAdsPlatformDataConversation**](LinkedInAdsPlatformDataConversation.md)> |  | [optional]
**event** | Option<[**models::LinkedInAdsPlatformDataEvent**](LinkedInAdsPlatformDataEvent.md)> |  | [optional]
**thought_leader** | Option<[**models::LinkedInAdsPlatformDataThoughtLeader**](LinkedInAdsPlatformDataThoughtLeader.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


