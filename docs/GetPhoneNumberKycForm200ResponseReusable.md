# Zernio.Model.GetPhoneNumberKycForm200ResponseReusable
Present when this account already has an approved verification for the country that can be reused (skip the form). `fromPhoneNumber`/`details` mirror the newest option; `options` lists ALL approved verifications (agencies hold one per end client) — pass the chosen option's `fromPhoneNumber` as `reuseFrom` on POST.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Available** | **bool** |  | [optional] 
**FromPhoneNumber** | **string** |  | [optional] 
**Details** | [**List&lt;GetPhoneNumberKycForm200ResponseReusableDetailsInner&gt;**](GetPhoneNumberKycForm200ResponseReusableDetailsInner.md) | Human-readable summary of the verification on file (field labels + values, plus the address as one line). Best-effort — may be empty if the provider lookup fails. | [optional] 
**Options** | [**List&lt;GetPhoneNumberKycForm200ResponseReusableOptionsInner&gt;**](GetPhoneNumberKycForm200ResponseReusableOptionsInner.md) | One entry per distinct approved verification, newest first. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

