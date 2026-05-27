# Zernio.Model.CreateWhatsAppFlowRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | WhatsApp social account ID | 
**Name** | **string** | Flow display name | 
**Categories** | **List&lt;CreateWhatsAppFlowRequest.CategoriesEnum&gt;** | Flow categories | 
**CloneFlowId** | **string** | Optional: ID of an existing flow to clone the Flow JSON from | [optional] 
**AsVersion** | **bool** | When cloning, true keeps the clone in cloneFlowId&#39;s version lineage (auto-numbered next version); false/absent creates an independent flow. Ignored without cloneFlowId. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

