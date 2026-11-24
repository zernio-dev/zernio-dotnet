# Zernio.Model.ConnectCustomDomain

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** |  | 
**Hostname** | **string** | The subdomain, such as &#x60;connect.yourbrand.com&#x60;. | 
**Zone** | **string** | The registered domain the records live in, such as &#x60;yourbrand.com&#x60;. | 
**Status** | **string** | &#x60;pending&#x60; until the TXT record is found and the certificate is issued, &#x60;active&#x60; once the domain serves the connect screens, &#x60;failed&#x60; when it stopped pointing at Zernio (remove it and add it again). | 
**ConnectEnabled** | **bool** | Whether new connect links open on this domain while it is active. | 
**OwnershipVerified** | **bool** | True once the TXT record was found. | 
**Records** | [**List&lt;ConnectCustomDomainRecordsInner&gt;**](ConnectCustomDomainRecordsInner.md) | The DNS records to add at your DNS provider. | 
**ActivatedAt** | **DateTime?** |  | 
**CreatedAt** | **DateTime** |  | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

