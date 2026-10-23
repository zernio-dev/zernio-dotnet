# Zernio.Model.ConnectHandoffLink
Only with `handoff=true`: the link to show as a QR code.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **Guid** | Pass to &#x60;GET /v1/connect/handoffs/{handoffId}&#x60;. | [optional] 
**Url** | **string** | Short link to encode in the QR code. It opens the welcome screen on the phone. | [optional] 
**ExpiresAt** | **DateTime** | When &#x60;url&#x60; stops working (30 minutes). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

