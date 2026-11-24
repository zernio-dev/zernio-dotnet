# Zernio.Model.GetEventsOverview200ResponseSitesInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**SiteId** | **string** |  | [optional] 
**ProfileId** | **string** | The profile the site belongs to. | [optional] 
**HitsToday** | **int** | Hits today. | [optional] 
**LastActiveOn** | **DateOnly?** | The last day in the past 7 with a hit. &#x60;null&#x60; when none. | [optional] 
**EventNamesLastWeek** | **List&lt;string&gt;** | Each event name people (not bots) sent the site in the last 7 days, sorted. Names the site sends that are neither standard nor in its &#x60;customEvents&#x60; are left out. | [optional] 
**Totals** | [**GetEventsOverview200ResponseSitesInnerTotals**](GetEventsOverview200ResponseSitesInnerTotals.md) |  | [optional] 
**SendsNowhere** | **bool** | Whether no forwarding rule of the profile to an ad platform uses the site (its own events, or server events its visits complete) and its tag fires no ad pixel in the browser. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

