# ListAdAccounts200ResponseAccountsInnerFundingSourceDetails

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | Option<**String**> | Meta's ID for the funding instrument. Matches `fundingSource`. | [optional]
**display_string** | Option<**String**> | Meta's own human-readable label for the funding instrument, e.g. 'Available Balance (EUR)' or a masked card. Meta composes this string; do not parse it. | [optional]
**r#type** | Option<**i32**> | Meta's raw numeric funding-source type, forwarded unchanged. Meta publishes no mapping from these numbers to payment-method kinds, so none is documented here and none should be inferred. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


