# Zernio.Model.WebhookPayloadSequenceEnrollment

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Test** | **bool** | Always true when present: only a sample sent by POST /v1/webhooks/test with an event carries it. Real deliveries never do. | [optional] 
**Id** | **string** | Event id, the dedupe key. | 
**Event** | **string** |  | 
**Timestamp** | **DateTime** |  | 
**Sequence** | [**UpdateFacebookPage200ResponseSelectedPage**](UpdateFacebookPage200ResponseSelectedPage.md) |  | 
**Contact** | [**WebhookPayloadContactTagContact**](WebhookPayloadContactTagContact.md) |  | 
**Enrollment** | [**CreateTestLead200ResponseTestLead**](CreateTestLead200ResponseTestLead.md) |  | 
**ExitReason** | **string** | sequence.exited only. completed: the last step was sent; replied: the contact replied and the sequence exits on reply; manual: unenrolled through the API; failed: the step kept failing to send; unsubscribed: the contact opted out. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

