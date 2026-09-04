# CreateStandaloneAdRequestPlatformSpecificData

## Enum Variants

| Name | Description |
|---- | -----|
| LinkedInAdsPlatformData | Platform-specific options. The platform is derived from &#x60;accountId&#x60;; sending options for a different platform returns a 400. LinkedIn (campaign bidding and delivery controls) and Meta (the bid trio) have options today.  **Meta**: &#x60;bidStrategy&#x60;, &#x60;bidAmount&#x60; and &#x60;roasAverageFloor&#x60; may be sent here instead of at the root — the preferred home going forward. Sending the bid fields in BOTH places returns a 400 (&#x60;mutually_exclusive_fields&#x60;), and sending any of them in &#x60;adSetId&#x60; attach mode is a 400 too (the ad set already has its bid). &#x60;dailyMinSpendTarget&#x60; / &#x60;lifetimeMinSpendTarget&#x60; set the new ad set&#39;s minimum spend and live here only; they are rejected in &#x60;adSetId&#x60; attach mode as well.  |
| MetaAdsPlatformData | Platform-specific options. The platform is derived from &#x60;accountId&#x60;; sending options for a different platform returns a 400. LinkedIn (campaign bidding and delivery controls) and Meta (the bid trio) have options today.  **Meta**: &#x60;bidStrategy&#x60;, &#x60;bidAmount&#x60; and &#x60;roasAverageFloor&#x60; may be sent here instead of at the root — the preferred home going forward. Sending the bid fields in BOTH places returns a 400 (&#x60;mutually_exclusive_fields&#x60;), and sending any of them in &#x60;adSetId&#x60; attach mode is a 400 too (the ad set already has its bid). &#x60;dailyMinSpendTarget&#x60; / &#x60;lifetimeMinSpendTarget&#x60; set the new ad set&#39;s minimum spend and live here only; they are rejected in &#x60;adSetId&#x60; attach mode as well.  |

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


