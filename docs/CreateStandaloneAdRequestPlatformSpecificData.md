# CreateStandaloneAdRequestPlatformSpecificData

## Enum Variants

| Name | Description |
|---- | -----|
| LinkedInAdsPlatformData | Platform-specific options. The platform is derived from &#x60;accountId&#x60;; options for a different platform return a 400. LinkedIn (campaign bidding and delivery controls) and Meta (the bid trio) have options today.  **Meta**  - &#x60;bidStrategy&#x60;, &#x60;bidAmount&#x60; and &#x60;roasAverageFloor&#x60; may be sent here instead of at the root (the preferred home going forward). Sending them in BOTH places returns a 400 (&#x60;mutually_exclusive_fields&#x60;). - Sending any bid field in &#x60;adSetId&#x60; attach mode is a 400 (the ad set already has its bid). - &#x60;dailyMinSpendTarget&#x60; / &#x60;lifetimeMinSpendTarget&#x60; set the new ad set&#39;s minimum spend and live here only; also rejected in &#x60;adSetId&#x60; attach mode.  |
| MetaAdsPlatformData | Platform-specific options. The platform is derived from &#x60;accountId&#x60;; options for a different platform return a 400. LinkedIn (campaign bidding and delivery controls) and Meta (the bid trio) have options today.  **Meta**  - &#x60;bidStrategy&#x60;, &#x60;bidAmount&#x60; and &#x60;roasAverageFloor&#x60; may be sent here instead of at the root (the preferred home going forward). Sending them in BOTH places returns a 400 (&#x60;mutually_exclusive_fields&#x60;). - Sending any bid field in &#x60;adSetId&#x60; attach mode is a 400 (the ad set already has its bid). - &#x60;dailyMinSpendTarget&#x60; / &#x60;lifetimeMinSpendTarget&#x60; set the new ad set&#39;s minimum spend and live here only; also rejected in &#x60;adSetId&#x60; attach mode.  |

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


