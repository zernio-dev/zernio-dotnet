# Zernio.Model.StartSmsRegistrationRequestCampaign
Required for 10DLC. What you'll send and how recipients opt in/out. Opt-in/opt-out/help auto-responses must name the registered brand and carry the carrier-required disclosures; submissions that don't (or that are blank) are automatically rewritten to a compliant, brand-named template before the campaign is filed. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Usecase** | **string** |  | 
**SubUsecases** | **List&lt;StartSmsRegistrationRequestCampaign.SubUsecasesEnum&gt;** | The concrete kinds of messages a MIXED campaign sends (the carrier registry requires 2-5, and reviewers match them against the sample messages). Omitted: a default pair is applied for MIXED.  | [optional] 
**Description** | **string** |  | 
**MessageFlow** | **string** | How a recipient ends up receiving your messages (the opt-in flow). Include a link to the page or form where they opt in — carrier reviewers reject campaigns whose consent they can&#39;t verify. | 
**Sample1** | **string** |  | 
**Sample2** | **string** | Second example message; carriers require two distinct samples | 
**HelpMessage** | **string** |  | 
**OptinKeywords** | **string** |  | 
**OptinMessage** | **string** |  | 
**OptoutKeywords** | **string** |  | 
**OptoutMessage** | **string** |  | 
**HelpKeywords** | **string** |  | 
**EmbeddedLink** | **bool** |  | [optional] 
**EmbeddedPhone** | **bool** |  | [optional] 
**NumberPool** | **bool** |  | [optional] 
**AgeGated** | **bool** |  | [optional] 
**DirectLending** | **bool** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

