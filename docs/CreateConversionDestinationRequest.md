# CreateConversionDestinationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ad_account_id** | **String** | Ad account ID. For LinkedIn: numeric (e.g. \"5123456\") or full `urn:li:sponsoredAccount:{id}` URN. For Google: numeric customer ID (e.g. \"1234567890\") or `customers/{id}` form.  | 
**name** | **String** |  | 
**r#type** | **String** | Conversion type. For LinkedIn: a unified standard event name (e.g. \"Purchase\", \"Lead\", \"AddToCart\") or a LinkedIn rule type enum (e.g. \"PURCHASE\", \"QUALIFIED_LEAD\"). For Google: a unified standard event name (Purchase, Subscribe, CompleteRegistration, Lead, Schedule) or a Google ConversionActionCategory enum value directly (e.g. \"PURCHASE\", \"SUBSCRIBE_PAID\", \"SIGNUP\", \"IMPORTED_LEAD\", \"BOOK_APPOINTMENT\"). Unknown values pass through to the platform.  | 
**attribution_type** | Option<**AttributionType**> | LinkedIn only. (enum: LAST_TOUCH_BY_CAMPAIGN, LAST_TOUCH_BY_CONVERSION) | [optional]
**post_click_attribution_window_size** | Option<**PostClickAttributionWindowSize**> | LinkedIn only. Default 30. 365 only allowed for LEAD, PURCHASE, ADD_TO_CART, QUALIFIED_LEAD, SUBMIT_APPLICATION rule types; the API rejects other combinations locally.  (enum: 1, 7, 30, 90, 365) | [optional]
**view_through_attribution_window_size** | Option<**ViewThroughAttributionWindowSize**> | LinkedIn only. Default 7. Same 365-day-window type restriction applies as `postClickAttributionWindowSize`.  (enum: 1, 7, 30, 90, 365) | [optional]
**value_type** | Option<**ValueType**> | LinkedIn only. DYNAMIC (default) uses the per-event `value` from `sendConversions`. FIXED uses the rule's `value` field. NO_VALUE drops monetary value entirely.  (enum: DYNAMIC, FIXED, NO_VALUE) | [optional]
**value** | Option<[**models::CreateConversionDestinationRequestValue**](CreateConversionDestinationRequestValue.md)> |  | [optional]
**auto_association_type** | Option<**AutoAssociationType**> | LinkedIn only. Controls campaign association at rule-creation time: - ALL_CAMPAIGNS: associate the rule with every active,   paused, and draft campaign in the ad account - OBJECTIVE_BASED: associate only campaigns whose   objective matches the rule's type - NONE: don't auto-associate. Manage associations via   the `/associations` endpoints below. Note: auto-association runs once at create time; new campaigns added after the rule still need explicit association.  (enum: ALL_CAMPAIGNS, OBJECTIVE_BASED, NONE) | [optional][default to AllCampaigns]
**counting_type** | Option<**CountingType**> | Google Ads only. Whether to count multiple conversions from the same click (MANY_PER_CLICK) or at most one (ONE_PER_CLICK). Defaults to MANY_PER_CLICK if omitted.  (enum: MANY_PER_CLICK, ONE_PER_CLICK) | [optional]
**primary_for_goal** | Option<**bool**> | Google Ads only. When true, the conversion action is marked as primary and immediately influences Smart Bidding. Defaults to false (secondary, record-only) to avoid unintentionally steering the customer's campaigns on creation.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


