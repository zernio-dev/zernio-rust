# PurchasePhoneNumberRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**profile_id** | **String** | Profile to associate the number with | 
**country** | Option<**String**> | ISO 3166-1 alpha-2 country for the number (default US). International numbers require usage-based billing. Tier 3/4 countries return 202 { status: \"kyc_required\", kycUrl } — the customer must complete KYC at that URL before the number is ordered. See GET /v1/phone-numbers/countries.  | [optional][default to US]
**number_type** | Option<**NumberType**> | Which of the country's offered number types to order (see `types[]` on GET /v1/phone-numbers/countries). Omitted = the country's default type, which is always the WhatsApp-safe choice. Capabilities, price, and KYC requirements are per (country, type): toll_free can never connect WhatsApp (400 when combined with connectWhatsapp:true), and wantsSms:true requires an SMS-capable type.  (enum: local, mobile, national, toll_free) | [optional]
**connect_whatsapp** | Option<**bool**> | A phone number is the unit; WhatsApp is one optional feature. Pass false to buy a STANDALONE number (Calls/SMS only): provisioning skips the Meta pre-verify/OTP steps and the number activates immediately. Omitted defaults to the WhatsApp provisioning path. WhatsApp can be connected to a standalone number later from the connect flow.  | [optional][default to true]
**wants_sms** | Option<**bool**> | SMS capability is per-number, not per-country. Pass true to provision from the SMS-capable inventory pool so the number can actually text (see also GET /v1/phone-numbers/available with sms=true, and smsAvailable on GET /v1/phone-numbers/countries).  | [optional][default to false]
**wants_whatsapp** | Option<**bool**> | Declare WhatsApp intent on a STANDALONE purchase (connectWhatsapp:false). The number still activates and bills immediately, but if WhatsApp's buy-time check rejects the assigned number, it is automatically swapped for a WhatsApp-eligible one during the purchase instead of being delivered with WhatsApp unavailable. Ignored on the WhatsApp provisioning path (connectWhatsapp omitted or true), which always delivers a WhatsApp-verified number.  | [optional][default to false]
**purchase_intent_id** | Option<**String**> | Optional idempotency key. Send the same value when retrying a purchase: if a number was already bought under this key, the API returns { status: \"already_purchased\", numberId, phoneNumber } instead of provisioning a second number. Generate a fresh key for each genuinely new purchase.  | [optional]
**allow_multiple** | Option<**bool**> | Any second purchase within 10 minutes of a previous one is rejected with 409 code PURCHASE_VELOCITY as duplicate protection. Pass true to confirm the additional purchase is intentional (e.g. bulk provisioning).  | [optional][default to false]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


