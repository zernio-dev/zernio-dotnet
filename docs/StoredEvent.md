# Zernio.Model.StoredEvent

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EventId** | **string** |  | [optional] 
**ProfileId** | **string** | The profile the event was stored under. | [optional] 
**Source** | **string** | Where the event came from: &#x60;api&#x60;, &#x60;relay&#x60;, &#x60;web&#x60;, &#x60;shopify&#x60;, &#x60;woocommerce&#x60;, &#x60;stripe&#x60;, &#x60;hubspot&#x60;, &#x60;salesforce&#x60;, &#x60;gohighlevel&#x60;, &#x60;meta_leads&#x60;, &#x60;google_leads&#x60;, &#x60;linkedin_leads&#x60;, &#x60;tiktok_leads&#x60;, &#x60;form_leads&#x60; (a website form or &#x60;POST /v1/leads&#x60;) or &#x60;postback&#x60; (an affiliate network&#39;s postback to a tracking link). | [optional] 
**EventName** | **string** |  | [optional] 
**EventTime** | **DateTime** |  | [optional] 
**ReceivedAt** | **DateTime** |  | [optional] 
**ActionSource** | **string** |  | [optional] 
**Value** | **decimal?** |  | [optional] 
**Currency** | **string** |  | [optional] 
**SourceUrl** | **string** | Origin, path and attribution parameters only. | [optional] 
**Utm** | [**StoredEventUtm**](StoredEventUtm.md) |  | [optional] 
**Zrn** | **string** | Ad ID from the &#x60;zrn&#x60; parameter Zernio adds to links of ads it creates. | [optional] 
**ClickIds** | [**StoredEventClickIds**](StoredEventClickIds.md) |  | [optional] 
**DestinationsSent** | **int** | Destinations the event was forwarded to. | [optional] 
**HasEmail** | **bool** |  | [optional] 
**HasPhone** | **bool** |  | [optional] 
**HasExternalId** | **bool** |  | [optional] 
**PairedEventId** | **string** | In a &#x60;GET /v1/events&#x60; page: the other copy of the same conversion, when a website tag (&#x60;web&#x60;) and a server send both stored it under different event ids (same event name, a shared identifier, at most 30 minutes apart). &#x60;null&#x60; otherwise, and always &#x60;null&#x60; from &#x60;GET /v1/events/{eventId}&#x60;. | [optional] 
**Ad** | [**StoredEventAd**](StoredEventAd.md) |  | [optional] 
**Campaign** | [**StoredEventCampaign**](StoredEventCampaign.md) |  | [optional] 
**Counted** | **bool** | &#x60;false&#x60; for a website (&#x60;web&#x60;) copy of an event name a server source also reported that day: the server copy counts in the overview and campaign results, and this one is kept but not counted. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

