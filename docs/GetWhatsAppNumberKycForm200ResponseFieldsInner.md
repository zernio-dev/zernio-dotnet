# Zernio.Model.GetWhatsAppNumberKycForm200ResponseFieldsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**RequirementId** | **string** |  | [optional] 
**Label** | **string** |  | [optional] 
**Kind** | **string** | \&quot;action\&quot; &#x3D; an out-of-band verification (e.g. Onfido); not filled here, fulfilled after the order via a link. | [optional] 
**Description** | **string** | Plain-English explanation of what to provide. | [optional] 
**Example** | **string** | Concrete example value. | [optional] 
**LocalTo** | **string** | ISO country the value must be local to | [optional] 
**Audience** | **string** | When set, the requirement applies ONLY to this end-user type — provide it for that type and OMIT it for the other (e.g. Brazil: \&quot;Cartão CNPJ\&quot; is business-only, \&quot;CPF\&quot; and \&quot;ID/Passport Copy\&quot; are personal-only). Submitting both sets makes the regulator ask whether the number is for personal or business use and stalls the review. Pass &#x60;entityType&#x60; on POST so the server drops the inapplicable set. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

