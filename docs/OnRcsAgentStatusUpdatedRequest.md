# Zernio.Model.OnRcsAgentStatusUpdatedRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Stable webhook event ID: the dedupe key, also sent as the X-Zernio-Event-Id header and identical on every retry and redelivery. It identifies the event only, never an account or other resource. | [optional] 
**Event** | **string** |  | [optional] 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | [optional] 
**Agent** | [**OnRcsAgentStatusUpdatedRequestAgent**](OnRcsAgentStatusUpdatedRequestAgent.md) |  | [optional] 
**Status** | **string** |  | [optional] 
**Reason** | **string** | Our review note on changes_requested, the reason on rejected, or why a launch filing bounced back to testing. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

