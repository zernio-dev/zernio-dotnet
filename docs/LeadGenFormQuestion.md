# Zernio.Model.LeadGenFormQuestion
A single question on a Meta Instant Form. The `type` enum spans Meta's prefill set (FULL_NAME, EMAIL, PHONE, STREET_ADDRESS, CITY, STATE, COUNTRY, POST_CODE, DOB, GENDER, JOB_TITLE, COMPANY_NAME, etc.) plus custom types (CUSTOM, MULTIPLE_CHOICE, CONDITIONAL, STORE_LOOKUP, APPOINTMENT_REQUEST). See Meta's Lead Ads docs for the full list — we forward whatever string the caller sends so new types work without a Zernio release. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Key** | **string** | Stable key returned in &#x60;field_data&#x60; on each lead. If omitted, Meta auto-derives one from &#x60;label&#x60;. | [optional] 
**Label** | **string** | Display text shown above the input. | [optional] 
**Type** | **string** |  | 
**Options** | [**List&lt;LeadGenFormQuestionOptionsInner&gt;**](LeadGenFormQuestionOptionsInner.md) | Required for MULTIPLE_CHOICE / CONDITIONAL questions. | [optional] 
**InlineContext** | **string** | Help text rendered below the field. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

