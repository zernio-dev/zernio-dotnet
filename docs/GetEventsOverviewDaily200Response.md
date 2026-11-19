# Zernio.Model.GetEventsOverviewDaily200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Period** | **string** |  | [optional] 
**Totals** | [**GetEventsOverviewDaily200ResponseTotals**](GetEventsOverviewDaily200ResponseTotals.md) |  | [optional] 
**Days** | [**List&lt;GetEventsOverviewDaily200ResponseDaysInner&gt;**](GetEventsOverviewDaily200ResponseDaysInner.md) | Every day of the period, oldest first, zero where nothing happened. | [optional] 
**EventNames** | **List&lt;string&gt;** | The event names stored in the period, most events first. | [optional] 
**Platforms** | [**List&lt;GetEventsOverviewDaily200ResponsePlatformsInner&gt;**](GetEventsOverviewDaily200ResponsePlatformsInner.md) | Each platform events were sent to in the period, most sends first. | [optional] 
**PixelMissed** | [**List&lt;GetEventsOverviewDaily200ResponsePixelMissedInner&gt;**](GetEventsOverviewDaily200ResponsePixelMissedInner.md) | For each platform sent to in the period, the website conversions of people who allowed ad cookies (bots left out) and how many its browser pixel missed, which Zernio sent from its server. Most missed first; &#x60;null&#x60; without a tracked website in scope. | [optional] 
**Breakdown** | [**GetEventsOverviewDaily200ResponseBreakdown**](GetEventsOverviewDaily200ResponseBreakdown.md) |  | [optional] 
**Previous** | [**GetEventsOverviewDaily200ResponsePrevious**](GetEventsOverviewDaily200ResponsePrevious.md) |  | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

