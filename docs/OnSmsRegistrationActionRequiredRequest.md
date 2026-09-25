# Zernio.Model.OnSmsRegistrationActionRequiredRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**Event** | **string** |  | [optional] 
**Timestamp** | **DateTime** | UTC time at which Zernio generated this event (set once when the event payload is built, before delivery is queued). Retries and redeliveries keep the original value, so it reflects the event, not the delivery attempt. | [optional] 
**Registration** | [**OnSmsRegistrationActionRequiredRequestRegistration**](OnSmsRegistrationActionRequiredRequestRegistration.md) |  | [optional] 
**Reason** | **string** |  | [optional] 
**Message** | **string** | What to do, in words: our request or the carrier&#39;s note. Absent for otp_required. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

