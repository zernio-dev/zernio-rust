# InlineObject2Details

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**free_tier_account_limit** | Option<**i32**> | How many accounts the free tier allows. Only set when reason=free_tier_exceeded. | [optional]
**current_account_count** | Option<**i32**> | How many accounts the team currently has connected. Set when reason=free_tier_exceeded or reason=enterprise_required. | [optional]
**has_payment_method** | Option<**bool**> | Whether the team currently has a card on file in Stripe. Set when reason=free_tier_exceeded or reason=twitter_passthrough. | [optional]
**public_account_limit** | Option<**i32**> | Public pricing ceiling (the published cap beyond which an enterprise contract is required). Only set when reason=enterprise_required. | [optional]
**effective_account_limit** | Option<**i32**> | The cap actually applied to this team. Equals `public_account_limit` for organic teams; for teams with a per-customer override (grandfathered legacy customers, signed enterprise contracts) this can be higher. Only set when reason=enterprise_required.  | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


