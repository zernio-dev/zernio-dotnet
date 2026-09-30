# Zernio.Model.Verification
A managed OTP verification. The code itself is never returned or stored (hash only).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**Channel** | **string** |  | [optional] 
**To** | **string** |  | [optional] 
**ExpiresAt** | **DateTime** |  | [optional] 
**Attempts** | **int** |  | [optional] 
**MaxAttempts** | **int** |  | [optional] 
**SendCount** | **int** | Accepted deliveries (initial send + resends); each bills one verification fee. | [optional] 
**LastSentAt** | **DateTime?** |  | [optional] 
**DeliveryStatus** | **string** | WhatsApp only, returned by GET /v1/verify/verifications/{verificationId} (null on create and check responses): what Meta reported for the latest send, null until it reports. A code that never reached the recipient (for example a number not on WhatsApp) reads failed, with the Meta error in deliveryErrorCode. failed does not settle the verification: Meta can report failed and later deliver the same message. Reported for at least an hour after the send, well past any code&#39;s expiry. | [optional] 
**DeliveryErrorCode** | **int?** | Meta error code when deliveryStatus is failed (e.g. 131026, message undeliverable). | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 
**Resend** | **bool** | Present on create responses: true when an active verification was resent instead of created. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

