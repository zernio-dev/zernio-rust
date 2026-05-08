# CreateConversionDestinationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_account_id** | **String** | Sponsored ad account ID. Numeric (e.g. \"5123456\") or full `urn:li:sponsoredAccount:{id}` URN.  | 
**name** | **String** |  | 
**r#type** | **String** | Either a unified standard event name (e.g. \"Purchase\", \"Lead\", \"AddToCart\") or a LinkedIn rule type enum value (e.g. \"PURCHASE\", \"QUALIFIED_LEAD\"). The API maps standard names to LinkedIn enum values automatically.  | 
**attribution_type** | Option<**AttributionType**> |  (enum: LAST_TOUCH_BY_CAMPAIGN, LAST_TOUCH_BY_CONVERSION) | [optional]
**post_click_attribution_window_size** | Option<**PostClickAttributionWindowSize**> | Default 30. 365 only allowed for LEAD, PURCHASE, ADD_TO_CART, QUALIFIED_LEAD, SUBMIT_APPLICATION rule types — the API rejects other combinations locally.  (enum: 1, 7, 30, 90, 365) | [optional]
**view_through_attribution_window_size** | Option<**ViewThroughAttributionWindowSize**> | Default 7. Same 365-day-window type restriction applies as `postClickAttributionWindowSize`.  (enum: 1, 7, 30, 90, 365) | [optional]
**value_type** | Option<**ValueType**> | DYNAMIC (default) uses the per-event `value` from `sendConversions`. FIXED uses the rule's `value` field. NO_VALUE drops monetary value entirely.  (enum: DYNAMIC, FIXED, NO_VALUE) | [optional]
**value** | Option<[**models::CreateConversionDestinationRequestValue**](CreateConversionDestinationRequestValue.md)> |  | [optional]
**auto_association_type** | Option<**AutoAssociationType**> | Controls campaign association at rule-creation time: - ALL_CAMPAIGNS: associate the rule with every active,   paused, and draft campaign in the ad account - OBJECTIVE_BASED: associate only campaigns whose   objective matches the rule's type - NONE: don't auto-associate. Manage associations via   the `/associations` endpoints below. Note: auto-association runs once at create time; new campaigns added after the rule still need explicit association.  (enum: ALL_CAMPAIGNS, OBJECTIVE_BASED, NONE) | [optional][default to AllCampaigns]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


