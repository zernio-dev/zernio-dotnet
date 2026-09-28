# Zernio.Model.GetVoiceCallEstimate200ResponseBreakdown

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**TelnyxCostUSD** | **decimal** |  | [optional] 
**RecordingCostUSD** | **decimal** |  | [optional] 
**TranscriptionCostUSD** | **decimal** |  | [optional] 
**BrandedCallUSD** | **decimal** | Branded Calling surcharge, 0 unless &#x60;from&#x60; is a verified branded number calling a US destination. | [optional] 
**BillableCostUSD** | **decimal** | What Zernio bills for the call. | [optional] 
**TotalCostUSD** | **decimal** | Equals billableCostUSD (no separate Meta bill on PSTN); kept for shape parity with the WhatsApp estimate. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

