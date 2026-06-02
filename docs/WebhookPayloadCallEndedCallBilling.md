# Zernio.Model.WebhookPayloadCallEndedCallBilling

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**MetaCostUSD** | **decimal** | Meta per-minute charge. Billed by Meta DIRECTLY to your WhatsApp Business Account payment method (your separate Meta invoice). Zernio does NOT charge this. Display only. | [optional] 
**TelnyxCostUSD** | **decimal** |  | [optional] 
**RecordingCostUSD** | **decimal** |  | [optional] 
**BillableCostUSD** | **decimal** | The amount Zernio bills you &#x3D; Telnyx leg + recording. Excludes Meta (billed by Meta directly). | [optional] 
**TotalCostUSD** | **decimal** | Full economic cost incl. the Meta portion you pay directly (Meta + Telnyx + recording). Display only, not the Zernio-billed amount. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

