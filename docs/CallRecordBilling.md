# Zernio.Model.CallRecordBilling

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MetaMinutes** | **decimal** |  | [optional] 
**TelnyxSeconds** | **decimal** |  | [optional] 
**TranscriptionSeconds** | **decimal** |  | [optional] 
**TranscriptionCostUSD** | **decimal** |  | [optional] 
**MetaCostUSD** | **decimal** | WhatsApp channel only. Meta per-minute charge, billed by Meta directly to your WABA. Display only; not billed by Zernio. | [optional] 
**TelnyxCostUSD** | **decimal** |  | [optional] 
**RecordingCostUSD** | **decimal** |  | [optional] 
**BillableCostUSD** | **decimal** | Amount Zernio bills you &#x3D; telephony leg + recording + transcription (excludes any Meta portion). | [optional] 
**TotalCostUSD** | **decimal** | Full cost incl. any Meta portion you pay directly. Display only. | [optional] 
**Currency** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

