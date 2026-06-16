# Zernio.Model.GetWhatsAppPhoneNumbers200ResponseNumbersInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | [optional] 
**PhoneNumber** | **string** |  | [optional] 
**Country** | **string** |  | [optional] 
**Status** | **string** |  | [optional] 
**RegistrantName** | **string** | For regulated numbers, who it&#39;s registered for (company or person) — set from the submitted KYC. | [optional] 
**TelnyxOrderId** | **string** | Present once the number order has been placed (i.e. the requirement group was approved). Absent while still in identity review. | [optional] 
**MonthlyCents** | **int** | Per-country monthly price in cents ($2..$25). | [optional] 
**ProfileId** | **Object** |  | [optional] 
**ProvisionedAt** | **DateTime** |  | [optional] 
**MetaPreverifiedId** | **string** |  | [optional] 
**MetaVerificationStatus** | **string** |  | [optional] 
**OnfidoVerificationUrl** | **string** | For regulated (Tier 3/4) numbers with an Onfido ID-verification step — the link to forward to the end user. Set once the order is placed; null otherwise. Poll this field after submitting KYC. | [optional] 
**EndUserFirstName** | **string** |  | [optional] 
**EndUserLastName** | **string** |  | [optional] 
**RegulatoryDeclineReason** | **string** | Reviewer rejection reason when status is regulatory_declined. | [optional] 
**CreatedAt** | **DateTime** |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

