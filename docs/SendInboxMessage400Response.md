# Zernio.Model.SendInboxMessage400Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Error** | **string** |  | [optional] 
**Code** | **string** | Stable machine-readable reason. PLATFORM_LIMITATION covers a capability the platform does not offer (e.g. Bluesky and Reddit DMs reject media); MISSING_PARTICIPANT means the stored conversation has no recipient to send to; DIRECT_SEND_NOT_ELIGIBLE and DIRECT_SEND_BLOCKED mean the WhatsApp Business Account needs Meta to grant or restore Direct Send access; DIRECT_SEND_LIMITED is temporary, Meta lifts it on its own. | [optional] 
**PlatformError** | [**SendInboxMessage400ResponsePlatformError**](SendInboxMessage400ResponsePlatformError.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

