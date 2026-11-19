# Zernio.Model.GetEventsOverview200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Today** | [**GetEventsOverview200ResponseToday**](GetEventsOverview200ResponseToday.md) |  | [optional] 
**Platforms** | [**List&lt;GetEventsOverview200ResponsePlatformsInner&gt;**](GetEventsOverview200ResponsePlatformsInner.md) | One entry per forwarding rule of the profiles covered. | [optional] 
**Sources** | [**List&lt;GetEventsOverview200ResponseSourcesInner&gt;**](GetEventsOverview200ResponseSourcesInner.md) | Each source that stored an event in the last 30 days, most recent first. | [optional] 
**Website** | [**GetEventsOverview200ResponseWebsite**](GetEventsOverview200ResponseWebsite.md) |  | [optional] 
**Sites** | [**List&lt;GetEventsOverview200ResponseSitesInner&gt;**](GetEventsOverview200ResponseSitesInner.md) | Each tracking site of the profiles covered, with its activity. Hit counts are approximate distinct counts without bots. | [optional] 
**EventNames** | [**List&lt;GetEventsOverview200ResponseEventNamesInner&gt;**](GetEventsOverview200ResponseEventNamesInner.md) | Each event name stored in the 30 days before today and where it comes from. When a name comes from both the website tag and a server source, only the server copies count (in this overview, the daily overview and campaign results). | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

