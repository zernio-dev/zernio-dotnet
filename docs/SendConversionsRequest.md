# Zernio.Model.SendConversionsRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AccountId** | **string** | SocialAccount ID (metaads, googleads, or linkedinads). | 
**DestinationId** | **string** | Platform destination identifier. For Meta, the pixel/dataset ID. For Google, the conversion action resource name. For LinkedIn, the conversion rule ID or full &#x60;urn:lla:llaPartnerConversion:{id}&#x60; URN.  | 
**Events** | [**List&lt;ConversionEvent&gt;**](ConversionEvent.md) |  | 
**TestCode** | **string** | Meta &#x60;test_event_code&#x60; passthrough. Ignored by Google and LinkedIn. | [optional] 
**Consent** | [**SendConversionsRequestConsent**](SendConversionsRequestConsent.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

