# Zernio.Model.GetEventsOverview200ResponseWebsite
`null` when the profile has no tracking site. Hit counts are approximate distinct counts.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Steps** | [**List&lt;GetEventsOverview200ResponseWebsiteStepsInner&gt;**](GetEventsOverview200ResponseWebsiteStepsInner.md) | The funnel: page views, product views, add to cart, checkouts and purchases today. | [optional] 
**Recovered** | **int** | Purchases with ad consent for which no browser pixel fired, so only the server reported them. | [optional] 
**Conversions** | **int** | Purchases today. | [optional] 
**Consented** | **int** | Page views with ad storage consent. | [optional] 
**Visits** | **int** | Page views today. | [optional] 
**Bots** | **int** | Page views from bots. | [optional] 
**ServerPlatforms** | **List&lt;string&gt;** | Platforms of the forwarding rules that receive website events. | [optional] 

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)

