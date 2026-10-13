# UpdateAdSetRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**platform** | **Platform** |  (enum: facebook, instagram, tiktok, linkedin, pinterest, google, twitter, openai, reddit) | 
**budget** | Option<[**models::UpdateAdSetRequestBudget**](UpdateAdSetRequestBudget.md)> |  | [optional]
**status** | Option<**Status**> | Writes the ad set's own on/off switch (Meta: `configured_status`; X: the line item's `entity_status` ACTIVE / PAUSED), whatever delivery status its ads report. Omit if not toggling delivery state. (enum: active, paused) | [optional]
**name** | Option<**String**> | Rename the ad set (on X, the line item `name`). Platforms without a rename return 501. At least one of budget/status/bidStrategy/name is required. | [optional]
**bid_strategy** | Option<[**models::BidStrategy**](BidStrategy.md)> | Ad-set-level bid strategy. Overrides the campaign-level default. Supported on Meta (facebook, instagram), TikTok, and OpenAI. On TikTok the Meta-style enum is mapped to bid_type / bid_price / deep_bid_type automatically. On OpenAI, LOWEST_COST_WITH_BID_CAP and COST_CAP both map to the ad group's `bidding_config.max_bid_micros` (one knob covers both); LOWEST_COST_WITH_MIN_ROAS is rejected with 422 (OpenAI has no ROAS-based bidding). On X it writes the line item's `bid_strategy`: LOWEST_COST_WITHOUT_CAP = AUTO, LOWEST_COST_WITH_BID_CAP = MAX and COST_CAP = TARGET, with `bidAmount` as `bid_amount_local_micro`; LOWEST_COST_WITH_MIN_ROAS is rejected with 422. X decides which strategy the line item's objective allows (TARGET only on REACH, FOLLOWERS and WEBSITE_CLICKS, MAX not on REACH or FOLLOWERS). On Reddit, see the mapping in the description above (LOWEST_COST_WITH_MIN_ROAS returns 422). Other platforms (linkedin, pinterest, google) return 501 Not Implemented when bidStrategy is set.  | [optional]
**smart_targeting** | Option<[**models::UpdateAdSetRequestSmartTargeting**](UpdateAdSetRequestSmartTargeting.md)> |  | [optional]
**bid_amount** | Option<**f64**> | Bid cap in WHOLE currency units (USD: 5 = $5.00; JPY: 100 = ¥100). Required when bidStrategy is LOWEST_COST_WITH_BID_CAP or COST_CAP. Internally converted to Meta's smallest-denomination integer, or (on OpenAI and X) to micros (× 1,000,000). Meta only: may be sent alone, WITHOUT bidStrategy, to update the cap amount on an ad set whose parent campaign is COST_CAP or LOWEST_COST_WITH_BID_CAP (the strategy is inherited from the campaign and is left untouched).  | [optional]
**roas_average_floor** | Option<**f64**> | Minimum ROAS as a decimal multiplier (2.0 = 2.0x). Required when bidStrategy is LOWEST_COST_WITH_MIN_ROAS. Sent to Meta as `bid_constraints.roas_average_floor` × 10000. Not supported on OpenAI (422).  | [optional]
**value_rule_set_id** | Option<**String**> | Meta only (other platforms return 501). Value rule set to attach to this ad set, from `/v1/ads/value-rule-sets`. Sending a different id replaces the current association. To DETACH, send `valueRulesApplied: false` and omit this field.  | [optional]
**value_rules_applied** | Option<**bool**> | Meta only (other platforms return 501). `false` DETACHES the ad set's value rule set and must be sent WITHOUT `valueRuleSetId`; the combination returns 400. `true` is optional when attaching, since attachment is driven by `valueRuleSetId`, and requires it to be present.  | [optional]
**platform_specific_data** | Option<[**models::UpdateAdSetRequestPlatformSpecificData**](UpdateAdSetRequestPlatformSpecificData.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


