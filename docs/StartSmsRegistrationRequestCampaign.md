# Zernio.Model.StartSmsRegistrationRequestCampaign
Required for 10DLC. What you'll send and how recipients opt in/out. The opt-in/opt-out/help auto-responses (`optinMessage`, `optoutMessage`, `helpMessage`) are optional: when omitted, a compliant, brand-named template with the carrier-required disclosures is generated for you. If you do send them, they must name the registered brand and carry the disclosures — submissions that don't are rewritten to the compliant template before the campaign is filed. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Usecase** | **string** |  | 
**SubUsecases** | **List&lt;StartSmsRegistrationRequestCampaign.SubUsecasesEnum&gt;** | The concrete kinds of messages a MIXED campaign sends (the carrier registry requires 2-5, and reviewers match them against the sample messages). Omitted: a default pair is applied for MIXED.  | [optional] 
**Description** | **string** |  | 
**MessageFlow** | **string** | How a recipient ends up receiving your messages (the opt-in flow). Include a link to the page or form where they opt in — carrier reviewers reject campaigns whose consent they can&#39;t verify. | 
**Sample1** | **string** |  | 
**Sample2** | **string** | Second example message; carriers require two distinct samples | 
**HelpMessage** | **string** |  | [optional] 
**OptinKeywords** | **string** |  | 
**OptinMessage** | **string** |  | [optional] 
**OptoutKeywords** | **string** |  | 
**OptoutMessage** | **string** |  | [optional] 
**HelpKeywords** | **string** |  | 
**EmbeddedLink** | **bool** |  | [optional] 
**EmbeddedPhone** | **bool** |  | [optional] 
**NumberPool** | **bool** |  | [optional] 
**AgeGated** | **bool** |  | [optional] 
**DirectLending** | **bool** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

