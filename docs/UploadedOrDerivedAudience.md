# UploadedOrDerivedAudience

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **String** |  | 
**ad_account_id** | **String** | Platform ad account ID. Must start with act_ for Meta; bare platform id for others (Google customer id, X/TikTok/LinkedIn/Pinterest account id). | 
**name** | **String** |  | 
**description** | Option<**String**> |  | [optional]
**r#type** | **Type** |  (enum: customer_list, company_list, engagement, website, website_retargeting, lookalike) | 
**match_rules** | Option<[**Vec<models::UploadedOrDerivedAudienceMatchRulesInner>**](UploadedOrDerivedAudienceMatchRulesInner.md)> | Required for website_retargeting audiences (LinkedIn only). Each rule is a URL pattern; a member who visits any matching page enters the segment. Needs the LinkedIn Insight Tag installed on the customer's site — the segment only starts filling once the tag reports visits.  The response's `platformAudienceId` is the LinkedIn adSegment id, valid for downstream use. These segments appear in GET /v1/ads/audiences with  `type: website_retargeting` once LinkedIn has finished building them.  | [optional]
**source_type** | Option<**SourceType**> | Required for engagement audiences (LinkedIn only): what members engaged with — a video/leadgen/single-image ad campaign, a Company Page or an Event page.  (enum: VIDEO_ADS, LEAD_GEN_FORMS, ORGANIZATION_PAGES, EVENT_PAGES, SINGLE_IMAGE_ADS) | [optional]
**trigger** | Option<**String**> | Required for engagement audiences. The action, validated by LinkedIn against `sourceType`. Common values: VIDEO_ADS FIRST_QUARTILE / MIDPOINT / THIRD_QUARTILE / FULL_COMPLETE; LEAD_GEN_FORMS VIEW_FORM / LEAD_FORM_SUBMIT; ORGANIZATION_PAGES VIEW / CTA_CLICK; EVENT_PAGES RSVPED / VIDEO_VIEWED / ENGAGEMENT / CLICK.  | [optional]
**lookback_days** | Option<**LookbackDays**> | Required for engagement audiences. Rolling window. (enum: 30, 60, 90, 180, 365) | [optional]
**engagement_sources** | Option<**Vec<String>**> | Required for engagement audiences. Campaign URNs for the ad source types, organization URNs for pages and events. LinkedIn creates one rule per source, all sharing the same trigger and lookbackDays.  | [optional]
**companies** | Option<[**Vec<models::UploadedOrDerivedAudienceCompaniesInner>**](UploadedOrDerivedAudienceCompaniesInner.md)> | Required for company_list audiences (LinkedIn only): plain-text company rows for account targeting. Each row needs at least one identifier. LinkedIn recommends 1,000+ companies for a usable match rate and takes up to 48h to process the list.  | [optional]
**pixel_id** | Option<**String**> | Required for website audiences | [optional]
**retention_days** | Option<**i32**> | Required for website audiences | [optional]
**source_audience_id** | Option<**String**> | Required for lookalike audiences | [optional]
**country** | Option<**String**> | 2-letter code, required for lookalike audiences | [optional]
**ratio** | Option<**f64**> | Required for lookalike audiences | [optional]
**rule** | Option<**serde_json::Value**> | Pixel event rule for website audiences (optional) | [optional]
**customer_file_source** | Option<**String**> | Data source declaration for GDPR compliance (customer_list only) | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


