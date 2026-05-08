# Zernio.Model.CreateConversionDestinationRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**AdAccountId** | **string** | Sponsored ad account ID. Numeric (e.g. \&quot;5123456\&quot;) or full &#x60;urn:li:sponsoredAccount:{id}&#x60; URN.  | 
**Name** | **string** |  | 
**Type** | **string** | Either a unified standard event name (e.g. \&quot;Purchase\&quot;, \&quot;Lead\&quot;, \&quot;AddToCart\&quot;) or a LinkedIn rule type enum value (e.g. \&quot;PURCHASE\&quot;, \&quot;QUALIFIED_LEAD\&quot;). The API maps standard names to LinkedIn enum values automatically.  | 
**AttributionType** | **string** |  | [optional] 
**PostClickAttributionWindowSize** | **int** | Default 30. 365 only allowed for LEAD, PURCHASE, ADD_TO_CART, QUALIFIED_LEAD, SUBMIT_APPLICATION rule types — the API rejects other combinations locally.  | [optional] 
**ViewThroughAttributionWindowSize** | **int** | Default 7. Same 365-day-window type restriction applies as &#x60;postClickAttributionWindowSize&#x60;.  | [optional] 
**ValueType** | **string** | DYNAMIC (default) uses the per-event &#x60;value&#x60; from &#x60;sendConversions&#x60;. FIXED uses the rule&#39;s &#x60;value&#x60; field. NO_VALUE drops monetary value entirely.  | [optional] 
**Value** | [**CreateConversionDestinationRequestValue**](CreateConversionDestinationRequestValue.md) |  | [optional] 
**AutoAssociationType** | **string** | Controls campaign association at rule-creation time: - ALL_CAMPAIGNS: associate the rule with every active,   paused, and draft campaign in the ad account - OBJECTIVE_BASED: associate only campaigns whose   objective matches the rule&#39;s type - NONE: don&#39;t auto-associate. Manage associations via   the &#x60;/associations&#x60; endpoints below. Note: auto-association runs once at create time; new campaigns added after the rule still need explicit association.  | [optional] [default to AutoAssociationTypeEnum.ALLCAMPAIGNS]

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

