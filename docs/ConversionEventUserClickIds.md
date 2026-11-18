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
**Epik** | **string** | Pinterest click ID (the &#x60;epik&#x60; URL param or &#x60;_epik&#x60; cookie). Sent to Pinterest as &#x60;click_id&#x60;, not hashed. | [optional] 
**RdtCid** | **string** | Reddit click ID (the &#x60;rdt_cid&#x60; URL param Reddit adds to ad clicks). Sent to Reddit as &#x60;click_id&#x60;, not hashed. | [optional] 
**RdtUuid** | **string** | Reddit Pixel browser id (the &#x60;_rdt_uuid&#x60; first-party cookie). Sent to Reddit as &#x60;user.uuid&#x60;, not hashed. | [optional] 
**Aleid** | **string** | Axon (AppLovin) click id (the &#x60;aleid&#x60; URL param Axon adds to ad clicks, kept by its pixel in the &#x60;_axeid&#x60; cookie). Sent to Axon as &#x60;user_data.aleid&#x60;, not hashed. | [optional] 
**Alart** | **string** | Axon (AppLovin) attribution token (the &#x60;alart&#x60; URL param, &#x60;_axart&#x60; cookie). Sent to Axon as &#x60;user_data.alart&#x60;, not hashed. | [optional] 
**Axwrt** | **string** | Axon Pixel browser id (the &#x60;_axwrt&#x60; cookie). Sent to Axon as &#x60;user_data.axwrt&#x60;, not hashed. | [optional] 
**Twclid** | **string** | X click ID (the &#x60;twclid&#x60; URL param X adds to ad clicks). Sent to X as a &#x60;twclid&#x60; identifier, not hashed. | [optional] 
**Msclkid** | **string** | Microsoft Advertising click ID (the &#x60;msclkid&#x60; URL param Microsoft adds to ad clicks). Sent to Microsoft as &#x60;MicrosoftClickId&#x60;, not hashed. | [optional] 
**Sccid** | **string** | Snapchat click ID (the &#x60;ScCid&#x60; URL param Snap adds to ad clicks). Sent to Snapchat as &#x60;sc_click_id&#x60;, not hashed. | [optional] 
**Scid** | **string** | Snap Pixel browser id (the &#x60;_scid&#x60; cookie). Sent to Snapchat as &#x60;sc_cookie1&#x60;, not hashed. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

