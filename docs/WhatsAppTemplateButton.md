# Zernio.Model.WhatsAppTemplateButton

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Type** | **string** |  | 
**Text** | **string** | Visible button label. Required for all types except copy_code (whose label is fixed by WhatsApp) and otp (omit it and WhatsApp supplies its own label, localized to the template language; an English label on a non-English template is rejected). | [optional] 
**Url** | **string** | Required when type is URL | [optional] 
**Example** | **Object** |  | [optional] 
**PhoneNumber** | **string** | Required when type is phone_number | [optional] 
**OtpType** | **string** | Required when type is otp | [optional] 
**AutofillText** | **string** |  | [optional] 
**PackageName** | **string** |  | [optional] 
**SignatureHash** | **string** |  | [optional] 
**FlowId** | **string** |  | [optional] 
**FlowName** | **string** |  | [optional] 
**FlowJson** | **string** |  | [optional] 
**FlowAction** | **string** |  | [optional] 
**NavigateScreen** | **string** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

