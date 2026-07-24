# Zernio.Model.SubmitWhatsAppNumberKycRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ProfileId** | **string** |  | 
**Country** | **string** |  | 
**SubmissionId** | **string** | Idempotency token for this submission attempt. A retry/double-submit with the same token returns the same number; omit and each call creates a new number. | [optional] 
**Quantity** | **int** | Provision several same-country numbers from one submission (1-5). The single verification covers all of them; each number is billed only when it activates. Numbers that fail to order are skipped (best-effort). | [optional] [default to 1]
**Reuse** | **bool** | Reuse a prior approved verification for this country (skips document/field collection; places the order immediately). | [optional] 
**ReuseOptionId** | **string** | Which reusable verification to use (GET reusable.options[].id). The unambiguous selection key. Omitted &#x3D; the approved default. No match &#x3D; 409. | [optional] 
**ReuseFrom** | **string** | Legacy fallback for &#x60;reuseOptionId&#x60;: the source phone number (GET reusable.options[].fromPhoneNumber). Ambiguous when a number labels two verifications — prefer &#x60;reuseOptionId&#x60;. Omitted &#x3D; the approved default. No match &#x3D; 409. | [optional] 
**AreaCode** | **string** | Area code (NDC) the number must be in. Hard constraint: an empty area pool fails with 409 code AREA_CODE_UNAVAILABLE instead of ordering from another area. Omit for any area. Options come from GET /v1/phone-numbers/availability (areaOptions); the purchase 202 kycUrl echoes the areaCode picked at purchase time so it can be passed here. | [optional] 
**EndUserFirstName** | **string** | End user&#39;s legal first name. Required when the country has an action/ID-verification (Onfido) requirement. | [optional] 
**EndUserLastName** | **string** | End user&#39;s legal last name. Same condition as endUserFirstName. | [optional] 
**Values** | **Dictionary&lt;string, string&gt;** | requirementId → textual value | [optional] 
**Documents** | [**List&lt;SubmitWhatsAppNumberKycRequestDocumentsInner&gt;**](SubmitWhatsAppNumberKycRequestDocumentsInner.md) | One per document requirement. Each is EITHER inline base64 OR a &#x60;documentId&#x60; returned by POST /v1/whatsapp/phone-numbers/kyc/upload-document (use the upload endpoint for large files to stay under the request-size limit). | [optional] 
**Address** | [**SubmitPhoneNumberKycRequestAddress**](SubmitPhoneNumberKycRequestAddress.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

