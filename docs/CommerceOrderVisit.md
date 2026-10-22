# CommerceOrderVisit

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**occurred_at** | Option<**String**> | Null on WooCommerce, which records the session start without a timezone. | [optional]
**landing_url** | Option<**String**> | The first page of the session, with its query string. | [optional]
**referrer_url** | Option<**String**> |  | [optional]
**source** | Option<**String**> | Where the visit came from, as the platform names it. | [optional]
**source_type** | Option<**String**> | Shopify marketing tactic (e.g. SOCIAL, AD, SEARCH) or WooCommerce source type (utm, organic, referral, typein, admin). | [optional]
**utm** | Option<[**models::CommerceOrderVisitUtm**](CommerceOrderVisitUtm.md)> |  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


