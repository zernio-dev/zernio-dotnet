# Zernio.Model.AudienceUploadUser
One person. Each key is plaintext or its SHA-256 hash (64 hex characters). At least one key is required; see the endpoint description for which keys each platform uses.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Email** | **string** | Email, or SHA-256 of it trimmed and lowercased. | [optional] 
**Phone** | **string** | Phone with country code. Plaintext matches on Meta and Google; see the endpoint description before sending it hashed. | [optional] 
**FirstName** | **string** |  | [optional] 
**LastName** | **string** |  | [optional] 
**BirthYear** | **string** | YYYY. Meta only. | [optional] 
**BirthMonth** | **string** | MM (01-12). Meta only. | [optional] 
**BirthDay** | **string** | DD (01-31). Meta only. | [optional] 
**Gender** | **string** | m or f. Meta only. | [optional] 
**City** | **string** | Meta only. | [optional] 
**State** | **string** | Meta only. | [optional] 
**Zip** | **string** |  | [optional] 
**Country** | **string** | ISO 3166-1 alpha-2 code. | [optional] 
**ExternalId** | **string** | Your own id for the person. Meta only. | [optional] 
**Region** | **string** | Where the person is (ISO country, or US-CA). With no granted consent, EEA, UK and CH people are dropped before upload. | [optional] 
**Consent** | [**AudienceUploadUserConsent**](AudienceUploadUserConsent.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

