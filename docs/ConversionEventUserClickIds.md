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
**Msclkid** | **string** | Microsoft Advertising click ID (the &#x60;msclkid&#x60; URL param Microsoft adds to ad clicks). Sent to Microsoft as &#x60;MicrosoftClickId&#x60; (offline goals) or &#x60;userData.msclkid&#x60; (UET tags), not hashed. | [optional] 
**Sccid** | **string** | Snapchat click ID (the &#x60;ScCid&#x60; URL param Snap adds to ad clicks). Sent to Snapchat as &#x60;sc_click_id&#x60;, not hashed. | [optional] 
**Scid** | **string** | Snap Pixel browser id (the &#x60;_scid&#x60; cookie). Sent to Snapchat as &#x60;sc_cookie1&#x60;, not hashed. | [optional] 
**Tblci** | **string** | Taboola click ID (the &#x60;tblci&#x60; URL param Taboola adds to ad clicks with its &#x60;{click_id}&#x60; macro). Sent to Taboola as &#x60;click-id&#x60;, not hashed. | [optional] 
**Irclickid** | **string** | Impact partner click id (the &#x60;irclickid&#x60; URL param Impact adds to partner links). Sent to Impact as &#x60;ClickId&#x60;. | [optional] 
**Awc** | **string** | Awin click id (the &#x60;awc&#x60; URL param Awin adds to publisher links). Sent to Awin as the order&#39;s &#x60;awc&#x60;. | [optional] 
**Dclid** | **string** | Campaign Manager 360 / Display &amp; Video 360 click ID (the &#x60;dclid&#x60; URL param). Sent to Floodlight as is. | [optional] 
**Tdid** | **string** | The Trade Desk browser id (TDID) from a TTD cookie sync. Sent to The Trade Desk as &#x60;adid&#x60; of type &#x60;TDID&#x60;. | [optional] 
**Uid2** | **string** | A raw UID2 for the person, from your UID2 integration. Sent to The Trade Desk as &#x60;adid&#x60; of type &#x60;UID2&#x60;. | [optional] 
**Uid2Token** | **string** | A UID2 token (encrypted, from the UID2 SDK on your site). Sent to The Trade Desk as &#x60;uid2_token&#x60;. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

