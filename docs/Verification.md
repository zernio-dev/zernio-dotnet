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
**CreatedAt** | **DateTime** |  | [optional] 
**Resend** | **bool** | Present on create responses: true when an active verification was resent instead of created. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

