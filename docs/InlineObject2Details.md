# InlineObject2Details

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**free_tier_account_limit** | Option<**i32**> | How many accounts the free tier allows. Only set when reason=free_tier_exceeded. | [optional]
**current_account_count** | Option<**i32**> | How many accounts the team currently has connected. Set when reason=free_tier_exceeded or reason=enterprise_required. | [optional]
**has_payment_method** | Option<**bool**> | Whether the team currently has a card on file in Stripe. Set when reason=free_tier_exceeded or reason=twitter_passthrough. | [optional]
**effective_account_limit** | Option<**i32**> | The negotiated connected-account cap from the team's enterprise contract. Self-service teams have no cap and never receive this reason. Only set when reason=enterprise_required.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


