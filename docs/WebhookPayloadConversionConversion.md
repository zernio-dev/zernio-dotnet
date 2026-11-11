# Zernio.Model.WebhookPayloadConversionConversion

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**EventId** | **string** |  | 
**EventName** | **string** |  | 
**EventTime** | **DateTime** |  | 
**ReceivedAt** | **DateTime** |  | 
**Source** | **string** | Who sent it: &#x60;api&#x60;, &#x60;relay&#x60;, a lead form (&#x60;meta_leads&#x60;, &#x60;google_leads&#x60;, &#x60;linkedin_leads&#x60;, &#x60;tiktok_leads&#x60;), a store (&#x60;shopify&#x60;, &#x60;woocommerce&#x60;), &#x60;stripe&#x60; or &#x60;hubspot&#x60;. | 
**ActionSource** | **string** |  | [optional] 
**Value** | **decimal?** |  | [optional] 
**Currency** | **string** |  | [optional] 
**SourceUrl** | **string** | Origin, path and attribution parameters only. | [optional] 
**Utm** | [**StoredEventUtm**](StoredEventUtm.md) |  | [optional] 
**Zrn** | **string** |  | [optional] 
**ClickIds** | [**StoredEventClickIds**](StoredEventClickIds.md) |  | [optional] 
**DestinationsSent** | **int** |  | [optional] 
**HasEmail** | **bool** |  | [optional] 
**HasPhone** | **bool** |  | [optional] 
**HasExternalId** | **bool** |  | [optional] 
**Campaign** | [**WebhookPayloadConversionConversionCampaign**](WebhookPayloadConversionConversionCampaign.md) |  | 
**CampaignMatch** | **string** | &#x60;matched&#x60;, or why there is no campaign: &#x60;no_hint&#x60;, &#x60;no_campaign&#x60;, &#x60;ambiguous&#x60;, &#x60;not_counted&#x60; or &#x60;match_failed&#x60;. | 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

