# Zernio.Model.ConversionEventUserClickIds
Platform click identifiers captured from the originating ad click.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Fbc** | **string** | Meta click ID (from fbclid URL param). | [optional] 
**Fbp** | **string** | Meta browser ID (_fbp cookie). | [optional] 
**Gclid** | **string** | Google click ID (from gclid URL param). | [optional] 
**Gbraid** | **string** | Google iOS 14.5+ app attribution ID. | [optional] 
**Wbraid** | **string** | Google iOS 14.5+ web-to-app attribution ID. | [optional] 
**LiFatId** | **string** | LinkedIn first-party ad tracking click ID. Captured by parsing &#x60;li_fat_id&#x60; from landing-page URLs after the advertiser enables enhanced conversion tracking on the LinkedIn Insight Tag. Sent to LinkedIn as the LINKEDIN_FIRST_PARTY_ADS_TRACKING_UUID userId. Opaque token, not hashed.  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

