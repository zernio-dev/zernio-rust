# GetWhatsAppFlowsEncryptionKey200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**public_key** | Option<**String**> | The registered RSA public key in PEM format, or null when none is registered. | [optional]
**signature_status** | Option<**SignatureStatus**> | VALID (key matches Meta's records) or MISMATCH (no key registered, or the key does not match); null when unknown. (enum: VALID, MISMATCH) | [optional]
**registered** | Option<**bool**> | Whether a key is currently registered. Derived from publicKey, not signatureStatus. | [optional]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


