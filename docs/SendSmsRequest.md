# Zernio.Model.SendSmsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**From** | **string** | One of your SMS-enabled numbers (E.164; formatting is normalized). | 
**To** | **string** | Recipient number (E.164). | 
**Text** | **string** | Message body. Required unless &#x60;mediaUrls&#x60; is set. Max 10 SMS segments (1530 GSM-7 or 670 unicode characters). | [optional] 
**MediaUrls** | **List&lt;string&gt;** | Public media URLs to attach (sends as MMS). Max 10. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

