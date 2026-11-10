# CreatorCampaignCommissionTerms

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**percent_of_sales_bps** | Option<**i32**> | Share of the sales in basis points: 1500 is 15%. | [optional]
**per_order_cents** | Option<**i32**> | A flat amount per credited order. | [optional]
**attribution** | Option<**Attribution**> | How an order is credited: the creator's discount code, the last click on their tracking link, or both with the code winning. (enum: code_or_link, code, link) | [optional][default to CodeOrLink]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


