# Zernio.Model.ConversionEventUser
User identity fields. More signals mean higher match rates.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Email** | **string** | Plaintext email. Hashed server-side. | [optional] 
**Phone** | **string** | Phone number, ideally E.164. Hashed server-side. | [optional] 
**FirstName** | **string** | Plaintext first name. Hashed server-side. | [optional] 
**LastName** | **string** | Plaintext last name. Hashed server-side. | [optional] 
**ExternalId** | **string** | Stable customer identifier (e.g. CRM user ID). Hashed server-side for Meta and Google. Sent as plaintext to LinkedIn (LinkedIn&#39;s Conversions API spec requires the raw value). Maximum effective list size on LinkedIn is 1.  | [optional] 
**IpAddress** | **string** | Client IP address. Sent plaintext. | [optional] 
**UserAgent** | **string** | Client user-agent string. Sent plaintext. | [optional] 
**Country** | **string** | ISO 3166-1 alpha-2 country code, e.g. &#39;us&#39;. | [optional] 
**City** | **string** | Meta advanced matching (ct). Plaintext city; normalized + SHA-256 hashed server-side. Meta only. | [optional] 
**State** | **string** | Meta advanced matching (st). 2-letter ANSI for US; hashed server-side. Meta only. | [optional] 
**Zip** | **string** | Meta advanced matching (zp). US uses first 5 digits; hashed server-side. Meta only. | [optional] 
**Dob** | **string** | Meta advanced matching (db). YYYYMMDD; hashed server-side. Meta only. | [optional] 
**Gender** | **string** | Meta advanced matching (ge). &#39;f&#39; or &#39;m&#39;; hashed server-side. Meta only. | [optional] 
**ClickIds** | [**ConversionEventUserClickIds**](ConversionEventUserClickIds.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

