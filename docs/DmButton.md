# Zernio.Model.DmButton
A single inline button rendered inside an auto-DM via Meta's button_template. Up to 3 buttons per automation. `url` and `postback` work on Instagram and Facebook; `phone` is Facebook-only. When buttons are set, `dmMessage` becomes the button_template text and must be 640 characters or less. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**Title** | **string** | Button label (20 chars max) | 
**Url** | **string** | Target URL (required when type is url) | [optional] 
**Payload** | **string** | Postback payload delivered via the messaging_postbacks webhook (required when type is postback) | [optional] 
**Phone** | **string** | Phone number, e.g. +14155551234 (required when type is phone; Facebook only) | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

